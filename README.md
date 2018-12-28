# calculator
calculator
public class HesapMakinesi {
	
	
	static Scanner girilenler = new Scanner(System.in);
	static double hesap=0;
	//static double toplam=0;
	static String işlemci ="+";
	static String girilen ="";
	static String s ="";
	//static ArrayList<String> dizi = new ArrayList<String>();
	
	
	public static void main(String[] args) {//dizi.add("+");
		
		//getir();
	        while(!girilen.equals("=")) {
	        	System.out.println("sayı giriniz");
	        	getir();	
	        	//if(isNumeric(girilen)&&!isNumeric(dizi.get(dizi.size()-1))) {dizi.add(girilen);System.out.println("işlemci giriniz");}
	        	//getir();
	        	//else if (isNumeric(dizi.get(dizi.size()-1))&&(girilen.equals("+") || girilen.equals("-") || girilen.equals("*") || girilen.equals("/"))) 
	        	//{dizi.add(girilen);System.out.println("sayı giriniz");}
	        	//else {System.out.println("hatalı giriş");}
        	
	        
	        	if (isNumeric(girilen))
	        	{	 if(işlemci.equals("+")){hesap = hesap+Double.parseDouble(girilen);s=s+işlemci+girilen;if(s.substring(0,1).equals("+")) {s=s.substring(1,s.length());}System.out.println("işlem="+s);}
	        	else if(işlemci.equals("-")){hesap = hesap-Double.parseDouble(girilen);s=s+işlemci+girilen;System.out.println("işlem="+s);}	
	        	else if(işlemci.equals("*")){hesap = hesap*Double.parseDouble(girilen);s="("+s+")"+işlemci+girilen;System.out.println("işlem="+s);}
	        	else if(işlemci.equals("/")){hesap = hesap/Double.parseDouble(girilen);s="("+s+")"+işlemci+girilen;System.out.println("işlem="+s);}
	        	else{System.out.println("işlemci seçiniz");}
	        	}
	        	
	        	else if(!s.equals("")&&(girilen.equals("+") || girilen.equals("-") || girilen.equals("*") || girilen.equals("/"))) {işlemci = girilen;}
	        	else if(girilen.equals("c")) {hesap =0;işlemci="+";s="";girilen="";System.out.println("işlem silindi");}
	        	else if(girilen.equals("=")) {System.out.println("sonuc="+hesap);}
	        	else {System.out.println("hatalı giriş");}
		        	
		        	
	//	        }dizi.remove(0);if(dizi.size()>1) {if(!isNumeric(dizi.get(dizi.size()-1))) {dizi.remove(dizi.size()-1);}}else{System.out.println("giriş yapılmadı");} 
	//	        for (int i=0;i<dizi.size();i++) {s+=dizi.get(i);} System.out.print(s);
	//	        
	//	       ////String[] dizi2=s.split("+");
	//	        for(int i=0;i<(s.split("+")).length;i++) {if(isNumeric(s.split("+")[i])) {toplam =toplam+Double.parseDouble(s.split("+")[i]);s.replaceAll(s.split("+")[i],"");}}
	//	        for(int i=0;i<(s.split("+")).length;i++) {if(isNumeric(s.split("+")[i])) {toplam =toplam+Double.parseDouble(s.split("+")[i]);s.replaceAll(s.split("+")[i],"");}}
	       
	        	
	        
	        
	        }    
	}

	public static boolean isNumeric(String str) {
		try {double d = Double.parseDouble(str);} 
		catch (NumberFormatException nfe) {return false;}
		return true;
	}

	public static String getir() {girilen = girilenler.next();return girilen;}
	
	
	
}
