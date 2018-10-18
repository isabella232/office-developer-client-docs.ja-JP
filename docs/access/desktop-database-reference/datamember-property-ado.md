---
<span data-ttu-id="e88d4-101"><<<<<<< ヘッド タイトル: DataMember プロパティ (ADO) TOCTitle: DataMember プロパティ (ADO) === タイトル: DataMember プロパティ (ADO) TOCTitle: DataMember プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e88d4-101"><<<<<<< HEAD title: DataMember Property (ADO) TOCTitle: DataMember Property (ADO) ======= title: DataMember property (ADO) TOCTitle: DataMember property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e88d4-102">マスターの ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) ms:contentKeyID: 48548787 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="e88d4-102">master ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15) ms:contentKeyID: 48548787 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e88d4-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e88d4-103"><<<<<<< HEAD</span></span>
# <a name="datamember-property-ado"></a><span data-ttu-id="e88d4-104">DataMember プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e88d4-104">DataMember Property (ADO)</span></span>
=======
# <a name="datamember-property-ado"></a><span data-ttu-id="e88d4-105">DataMember プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e88d4-105">DataMember property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e88d4-106">master</span><span class="sxs-lookup"><span data-stu-id="e88d4-106">master</span></span>

<span data-ttu-id="e88d4-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e88d4-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e88d4-108">[DataSource](datasource-property-ado.md) プロパティによって参照されるオブジェクトから取得するデータ メンバーの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="e88d4-108">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

<span data-ttu-id="e88d4-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e88d4-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="e88d4-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="e88d4-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="e88d4-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="e88d4-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="e88d4-112">master</span><span class="sxs-lookup"><span data-stu-id="e88d4-112">master</span></span>

<span data-ttu-id="e88d4-p101">**String** の値を設定または取得します。名前の大文字と小文字は区別されません。</span><span class="sxs-lookup"><span data-stu-id="e88d4-p101">Sets or returns a **String** value. The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="e88d4-115">解説</span><span class="sxs-lookup"><span data-stu-id="e88d4-115">Remarks</span></span>

<span data-ttu-id="e88d4-116">データ環境でのデータ バインド コントロールを作成するのにはこのプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="e88d4-116">This property is used to create data-bound controls with the Data Environment.</span></span> <span data-ttu-id="e88d4-117">*.* の[Recordset](recordset-object-ado.md)オブジェクトとして表されるオブジェクト (*データ メンバー*) の名前を格納しているデータ (データ ソース) のコレクションを管理します。</span><span class="sxs-lookup"><span data-stu-id="e88d4-117">The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="e88d4-118">**DataMember** プロパティと **DataSource** プロパティは組み合わせて使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e88d4-118">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="e88d4-p103">**DataMember** プロパティは、 **DataSource** プロパティに指定されたどのオブジェクトを **Recordset** オブジェクトとして表すかを指定します。 **Recordset** オブジェクトは、このプロパティを設定する前に閉じておく必要があります。 **DataSource** プロパティの前に **DataMember** プロパティが設定されていない場合、または **DataMember** 名が、 **DataSource** プロパティに指定されているオブジェクトに認識されない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e88d4-p103">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object. The **Recordset** object must be closed before this property is set. An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="e88d4-122">**使用例**</span><span class="sxs-lookup"><span data-stu-id="e88d4-122">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
