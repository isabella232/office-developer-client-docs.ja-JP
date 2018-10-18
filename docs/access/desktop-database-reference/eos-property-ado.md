---
<span data-ttu-id="b8463-101">タイトル: EOS プロパティ (ADO のデスクトップのデータベース参照のアクセス)) <<<<<<< ヘッド TOCTitle: EOS プロパティ (ADO) === TOCTitle: EOS プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="b8463-101">title: EOS Property (ADO - Access desktop database reference)) <<<<<<< HEAD TOCTitle: EOS Property (ADO) ======= TOCTitle: EOS property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b8463-102">マスターの ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15) ms:contentKeyID: 48546474 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="b8463-102">master ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15) ms:contentKeyID: 48546474 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="b8463-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="b8463-103"><<<<<<< HEAD</span></span>
# <a name="eos-property-ado"></a><span data-ttu-id="b8463-104">EOS プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="b8463-104">EOS Property (ADO)</span></span>
=======
# <a name="eos-property-ado"></a><span data-ttu-id="b8463-105">EOS プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="b8463-105">EOS property (ADO)</span></span>
>>>>>>> <span data-ttu-id="b8463-106">master</span><span class="sxs-lookup"><span data-stu-id="b8463-106">master</span></span>


<span data-ttu-id="b8463-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8463-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b8463-108">現在の位置がストリームの末尾にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8463-108">Indicates whether the current position is at the end of the stream.</span></span>

<span data-ttu-id="b8463-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="b8463-109"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="b8463-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="b8463-110">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="b8463-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="b8463-111">Return values</span></span>
>>>>>>> <span data-ttu-id="b8463-112">master</span><span class="sxs-lookup"><span data-stu-id="b8463-112">master</span></span>

<span data-ttu-id="b8463-p101">現在の位置がストリームの末尾かどうかを示すブール型 ( **Boolean** ) の値を返します。ストリームにバイトがなくなると **EOS** は **True** を返し、現在の位置の後にもバイトがあると **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="b8463-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="b8463-p102">ストリームの末尾の位置を設定するには、[SetEOS](seteos-method-ado.md) メソッドを使用します。現在の位置を確認するには、 [Position](position-property-ado.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b8463-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

