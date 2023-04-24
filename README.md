# ntucoursec-c-
some homeworks and quizs code in this course
  void add(Data x){
        Product_list[item_type]=x;
        cout <<"Added. Product:"<<x.product_name<<".\nSell price: "<<x.price<<"\n";
        item_type++;
    }
    //更新產品
    void update(Data x){
        for(int i=0;i<item_type;i++){
            if(strcmp(x.product_name,Product_list[i].product_name)==0){
                Product_list[i].price=x.price;
                cout <<"Updated. Product:"<<x.product_name<<".\nSell Price: "<<x.price<<"\n";
                break;
            }
        }
    }
    //賣出產品
    void sell(Data2 x){
        for(int i=0;i<item_type;i++){
            if(strcmp(x.product_name,Product_list[i].product_name)==0){
                Product_list[i].number_of_sold+=x.number;
                cout <<"Sold. Product:"<<x.product_name<<".\nNumber of sold: "<<x.number<<"\n";
                profit+=x.number*Product_list[i].price;
                total_item_sold+=x.number;
                break;
            }
        }
    }
    //顯示目前賣出產品的數量和目前的總利潤
    void display(){
        for(int i=0;i<item_type;i++){
            cout <<"Product:"<<Product_list[i].product_name<<".\nTotal number of sold: "<<Product_list[i].number_of_sold<<"\n";
        }
        cout <<"Total product sold: "<<total_item_sold<<"\nProfit: "<<profit<<"\n";
    }
};
 
typedef class Old_Farmer_Market OFM;
 
int main(){
    OFM Old;
    Old.business();
    cout <<"Welcome to Old Farmer Market, what can I help you?\n";
while(1){
    char ctrl;
    char Data,Data2;
    int  x1,x2;
    cin>>ctrl;
    cin>>x1;
    cin>>x2;
    //遺失的部分
    if(ctrl=='a'){
    	void add(Data,x1){
        	Product_list[item_type]=x;
        	cout <<"Added. Product:"<<x.product_name<<".\nSell price: "<<x.price<<"\n";
        	item_type++;
    	}
	}
	else(ctrl=='u'){
		update(Data x){
        for(int i=0;i<item_type;i++){
            if(strcmp(x.product_name,Product_list[i].product_name)==0){
                Product_list[i].price=x.price;
                cout <<"Updated. Product:"<<x.product_name<<".\nSell Price: "<<x.price<<"\n";
                break;
            }
        }
    }
		
	}
	else(ctrl=='s'){
		sell(Data2 x){
        for(int i=0;i<item_type;i++){
            if(strcmp(x.product_name,Product_list[i].product_name)==0){
                Product_list[i].number_of_sold+=x.number;
                cout <<"Sold. Product:"<<x.product_name<<".\nNumber of sold: "<<x.number<<"\n";
                profit+=x.number*Product_list[i].price;
                total_item_sold+=x.number;
                break;
            }
        }
    }
	}
	else(ctrl=='d'){
		display(){
        for(int i=0;i<item_type;i++){
            cout <<"Product:"<<Product_list[i].product_name<<".\nTotal number of sold: "<<Product_list[i].number_of_sold<<"\n";
        }
        cout <<"Total product sold: "<<total_item_sold<<"\nProfit: "<<profit<<"\n";
    }
		
	}
	else(ctrl=='q'){
		cout <<"Thanks for visiting Old Farmer Market. Wish you have a good day. Bye bye.";
		break;
	}
}
return 0;
}

