---
<span data-ttu-id="45f8c-101"><<<<<<< ヘッド タイトル: HelpContext、HelpFile プロパティ (ADO) TOCTitle: HelpContext、HelpFile プロパティ (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="45f8c-101"><<<<<<< HEAD title: HelpContext, HelpFile Properties (ADO) TOCTitle: HelpContext, HelpFile Properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="45f8c-102">HelpContext プロパティと HelpFile プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="45f8c-102">HelpContext, HelpFile Properties (ADO)</span></span>

<span data-ttu-id="45f8c-103">=== タイトル: HelpContext、HelpFile プロパティ (ADO) TOCTitle: HelpContext、HelpFile プロパティ (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 2018/10/17 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="45f8c-103">======= title: HelpContext, HelpFile properties (ADO) TOCTitle: HelpContext, HelpFile properties (ADO) ms:assetid: 8a79f994-f17c-2983-0593-095801be762e ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15) ms:contentKeyID: 48546194 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="45f8c-104">HelpContext、HelpFile プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="45f8c-104">HelpContext, HelpFile properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="45f8c-105">master</span><span class="sxs-lookup"><span data-stu-id="45f8c-105">master</span></span>

<span data-ttu-id="45f8c-106">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="45f8c-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="45f8c-107">[Error](error-object-ado.md) オブジェクトに関連するヘルプ ファイルおよびヘルプ トピックを示します。</span><span class="sxs-lookup"><span data-stu-id="45f8c-107">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="45f8c-108"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="45f8c-108"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="45f8c-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="45f8c-109">Return Values</span></span>

  - <span data-ttu-id="45f8c-110">**HelpContextID**: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( **Long** ) の値で返します。</span><span class="sxs-lookup"><span data-stu-id="45f8c-110">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

  - <span data-ttu-id="45f8c-111">**HelpFile**: ヘルプ ファイルへの完全なパスに評価される文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="45f8c-111">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="45f8c-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="45f8c-112">Return values</span></span>

- <span data-ttu-id="45f8c-113">**HelpContextID**: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( **Long** ) の値で返します。</span><span class="sxs-lookup"><span data-stu-id="45f8c-113">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="45f8c-114">**HelpFile**: ヘルプ ファイルへの完全なパスに評価される文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="45f8c-114">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>
>>>>>>> <span data-ttu-id="45f8c-115">master</span><span class="sxs-lookup"><span data-stu-id="45f8c-115">master</span></span>

## <a name="remarks"></a><span data-ttu-id="45f8c-116">解説</span><span class="sxs-lookup"><span data-stu-id="45f8c-116">Remarks</span></span>

<span data-ttu-id="45f8c-p101">**HelpFile** プロパティでヘルプ ファイルが指定されている場合、 **HelpContext** プロパティを使って特定のヘルプ トピックを自動的に表示できます。該当するヘルプ トピックがない場合、 **HelpContext** プロパティは 0 を返し、 **HelpFile** プロパティは長さ 0 の文字列 ("") を返します。</span><span class="sxs-lookup"><span data-stu-id="45f8c-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

