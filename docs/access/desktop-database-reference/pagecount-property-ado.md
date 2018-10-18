---
<<<<<<< ヘッド タイトル: PageCount プロパティ (ADO) TOCTitle: PageCount プロパティ (ADO) === タイトル: PageCount プロパティ (ADO) TOCTitle: PageCount プロパティ (ADO)
>>>>>>> マスターの ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: 48546609 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="pagecount-property-ado"></a>PageCount プロパティ (ADO)
=======
# <a name="pagecount-property-ado"></a>PageCount プロパティ (ADO)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

[Recordset](recordset-object-ado.md) オブジェクトに含まれるデータのページ数を示します。

<<<<<<< ヘッド
## <a name="return-value"></a>戻り値
=======
## <a name="return-value"></a>戻り値
>>>>>>> master

**Recordset** のページ数を示す長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**PageCount**プロパティのデータ ページの数を決定するが、**レコード セット**オブジェクトでは使用します。 *ページ*は、 [PageSize](pagesize-property-ado.md)プロパティの設定のと同じサイズのレコードのグループです。 **PageSize**の値よりも少ないレコードがあるため、最後のページが完了しない場合でも、 **PageCount**の値に追加ページとしてカウントします。 **Recordset**オブジェクトがこのプロパティをサポートしていない場合、値は**PageCount**は決められていないことを示す-1 になります。

ページ機能の詳細については、 **PageSize** プロパティおよび [AbsolutePage](absolutepage-property-ado.md) プロパティのトピックを参照してください。

