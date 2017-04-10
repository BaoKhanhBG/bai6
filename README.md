# bai6
int arr1[]={9,8,7,6,5,4,3,2,1,0};
		int arr2[]={9,8,7,6,5,4,3,2,1,0};
		int arr3[]={0,0,0,0,0,0,0,0,0,0,0};
		int kq[]={0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0};
		
		for(int i=0; i<arr2.length; i++)
		{
			int t=0;
			for(int j=0; j<arr3.length; j++)
			{
				t=t+(arr2[i]*arr1[j]);
				arr3[j]=t%10;
				t=t/10;
			}
			int x=0;
			for(int z=i;z<arr2.length+i;z++)
			{
			
				if(z>=i)
				{
					x=x+arr3[z-i]+kq[z];
					kq[z]=x%10;
					x=x/10;
				}
			}
		}
		
		for(int w=kq.length;w>0;w++)
		{
			System.out.println(kq[w]);
		}
