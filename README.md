#include <iostream>
#include <cstdlib>
#include <stdlib.h>
#include <conio.h> 
using namespace std;
struct node
{
  int num;
  node *next; 
};
 
	node *head=NULL;
	node *posisi; 
	int option=0;
  
void tambahawal(){
  node *baru;
  baru=new node;
  cout<<"Masukkan Data	: ";
  cin>>baru->num;
  baru->next=NULL;
  if(head==NULL){
    head=baru;
    head->next=NULL;
  }else{
    baru->next = head;
    head = baru;
  }
} 

void tambahakhir(){
  node *temp1, *temp2; 
  temp1 = new node; 
  cout<<"Masukkan angka: ";
  cin>>temp1->num;
  temp1->next=NULL; 
  if (head==NULL){
    head=temp1;
    posisi=head;
  }else{
    temp2=head;
    while(temp2->next!=NULL){
      temp2=temp2->next; 
    }
	temp2->next=temp1;
  }
} 

//void buat ubah lainnya

//int main
