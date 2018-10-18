---
<span data-ttu-id="61fd8-101"><<<<<<< ヘッド タイトル: データ ソース プロパティ (ADO) TOCTitle: データ ソース プロパティ (ADO) === タイトル: DataSource プロパティ (ADO) TOCTitle: DataSource プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="61fd8-101"><<<<<<< HEAD title: DataSource Property (ADO) TOCTitle: DataSource Property (ADO) ======= title: DataSource property (ADO) TOCTitle: DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="61fd8-102">マスターの ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: 48545087 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="61fd8-102">master ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15) ms:contentKeyID: 48545087 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="61fd8-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="61fd8-103"><<<<<<< HEAD</span></span>
# <a name="datasource-property-ado"></a><span data-ttu-id="61fd8-104">DataSource プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="61fd8-104">DataSource Property (ADO)</span></span>
=======
# <a name="datasource-property-ado"></a><span data-ttu-id="61fd8-105">DataSource プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="61fd8-105">DataSource property (ADO)</span></span>
>>>>>>> <span data-ttu-id="61fd8-106">master</span><span class="sxs-lookup"><span data-stu-id="61fd8-106">master</span></span>


<span data-ttu-id="61fd8-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="61fd8-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="61fd8-108">[Recordset](recordset-object-ado.md) オブジェクトとして表されるデータを持つオブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="61fd8-108">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="61fd8-109">解説</span><span class="sxs-lookup"><span data-stu-id="61fd8-109">Remarks</span></span>

<span data-ttu-id="61fd8-110">データ環境でのデータ バインド コントロールを作成するのにはこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="61fd8-110">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="61fd8-111">*.* の**Recordset**オブジェクトとして表されるオブジェクト (*データ メンバー*) の名前を格納しているデータ (データ ソース) のコレクションを管理します。</span><span class="sxs-lookup"><span data-stu-id="61fd8-111">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="61fd8-112">[DataMember](datamember-property-ado.md) プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61fd8-112">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="61fd8-113">参照されるオブジェクトには、 **IDataSource** インターフェイスを実装し、 **IRowset** インターフェイスを組み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="61fd8-113">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="61fd8-114">**使用例**</span><span class="sxs-lookup"><span data-stu-id="61fd8-114">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
