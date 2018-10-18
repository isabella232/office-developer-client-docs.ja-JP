---
<<<<<<< ヘッド タイトル: NumericScale と Precision プロパティの使用例 (vj++) TOCTitle: NumericScale と Precision プロパティの使用例 (vj++) === タイトル: NumericScale と Precision プロパティの使用例 (vj++) TOCTitle: NumericScale と精度プロパティの使用例 (vj++)
>>>>>>> マスターの ms:assetid: 9b6fc40c-b740-ede0-d69d-546eb5d40c95 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249707(v=office.15) ms:contentKeyID: 48546574 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="numericscale-and-precision-properties-example-vj"></a>NumericScale プロパティと Precision プロパティの使用例 (VJ++)
=======
# <a name="numericscale-and-precision-properties-example-vj"></a>NumericScale と Precision プロパティの使用例 (vj++)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

この例では、[NumericScale](numericscale-property-ado.md) プロパティと [Precision](precision-property-ado.md) プロパティを使って、***Pubs*** データベースの ***Discounts*** テーブル内にあるフィールドの小数点以下の桁数と精度を表示します。

```java 
 
// BeginNumericScaleJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class NumericScaleX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 NumericScaleX(); 
 System.exit(0); 
 } 
 
 // NumericScaleX function 
 
 static void NumericScaleX() 
 { 
 
 // Define ADO Objects. 
 Recordset rstDiscounts = null; 
 Field fldTemp = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider='sqloledb';Data Source='MySqlServer';" 
 + "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 int intLoop; 
 
 try 
 { 
 rstDiscounts = new Recordset(); 
 
 // Open recordset. 
 rstDiscounts.open("Discounts", strCnn, 
 AdoEnums.CursorType.FORWARDONLY, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TABLE); 
 
 // Display numeric scale and precision of 
 // numeric and small integer fields. 
 for ( intLoop=0; intLoop < 
 rstDiscounts.getFields().getCount();intLoop++) 
 { 
 fldTemp = rstDiscounts.getFields().getItem(intLoop); 
 if((fldTemp.getType()== AdoEnums.DataType.NUMERIC) | 
 (fldTemp.getType()== AdoEnums.DataType.SMALLINT)) 
 { 
 System.out.println("\nField: " 
 + fldTemp.getName()); 
 System.out.println("\nNumeric scale: " 
 + fldTemp.getNumericScale()); 
 System.out.println("\nPrecision: " 
 + fldTemp.getPrecision()); 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 } 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstDiscounts != null) 
 { 
 PrintProviderError(rstDiscounts.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstDiscounts != null) 
 if (rstDiscounts.getState() == 1) 
 rstDiscounts.close(); 
 } 
 
 } 
 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
// EndNumericScaleJ 
```

