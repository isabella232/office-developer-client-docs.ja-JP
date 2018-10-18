---
<span data-ttu-id="ea351-101"><<<<<<< ヘッド タイトル: MarshalOptions プロパティ (ADO) TOCTitle: MarshalOptions プロパティ (ADO) === タイトル: MarshalOptions プロパティ (ADO) TOCTitle: MarshalOptions プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea351-101"><<<<<<< HEAD title: MarshalOptions Property (ADO) TOCTitle: MarshalOptions Property (ADO) ======= title: MarshalOptions property (ADO) TOCTitle: MarshalOptions property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ea351-102">マスターの ms:assetid: dc9c4e94-0725-210d-8251-079054541142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15) ms:contentKeyID: 48548143 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ea351-102">master ms:assetid: dc9c4e94-0725-210d-8251-079054541142 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15) ms:contentKeyID: 48548143 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ea351-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="ea351-103"><<<<<<< HEAD</span></span>
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="ea351-104">MarshalOptions プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea351-104">MarshalOptions Property (ADO)</span></span>
=======
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="ea351-105">MarshalOptions プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea351-105">MarshalOptions property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ea351-106">master</span><span class="sxs-lookup"><span data-stu-id="ea351-106">master</span></span>


<span data-ttu-id="ea351-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea351-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ea351-108">どのレコードがサーバーにマーシャリングされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="ea351-108">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ea351-109">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="ea351-109">Settings And Return Values</span></span>

<span data-ttu-id="ea351-p101">[MarshalOptionsEnum](marshaloptionsenum.md) の値を設定または取得します。既定値は **adMarshalAll** です。</span><span class="sxs-lookup"><span data-stu-id="ea351-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea351-112">解説</span><span class="sxs-lookup"><span data-stu-id="ea351-112">Remarks</span></span>

<span data-ttu-id="ea351-113"><<<<<<< ヘッド、クライアント側の[Recordset](recordset-object-ado.md)を使用する場合、クライアント上で変更されたレコードに書き戻す、中間層またはマーシャ リングをパッケージ化し、インターフェイスを送信するという手法を使用して Web サーバースレッドまたはプロセスの境界を越えてメソッドのパラメーターです。</span><span class="sxs-lookup"><span data-stu-id="ea351-113"><<<<<<< HEAD When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or Web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="ea351-114">**スレッド**を設定すると、リモート データが変更されたが、中間層または Web サーバーに更新するためにマーシャ リングするときにパフォーマンスが向上することができます。</span><span class="sxs-lookup"><span data-stu-id="ea351-114">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or Web server.</span></span>
<span data-ttu-id="ea351-115">=== クライアント側の[Recordset](recordset-object-ado.md)を使用すると、クライアント上で変更されたレコードに書き込まれます戻る、中間層またはマーシャ リングをパッケージ化し、全体のインターフェイス メソッドのパラメーターを送信するという手法を使用して web サーバースレッドまたはプロセスの境界。</span><span class="sxs-lookup"><span data-stu-id="ea351-115">======= When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="ea351-116">**スレッド**を設定すると、リモート データが変更されたが、中間層または web サーバーに更新するためにマーシャ リングするときにパフォーマンスが向上することができます。</span><span class="sxs-lookup"><span data-stu-id="ea351-116">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>
>>>>>>> <span data-ttu-id="ea351-117">master</span><span class="sxs-lookup"><span data-stu-id="ea351-117">master</span></span>

<span data-ttu-id="ea351-118">**リモート データ サービスの使用法**このプロパティはクライアント側の**Recordset**でのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="ea351-118">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

