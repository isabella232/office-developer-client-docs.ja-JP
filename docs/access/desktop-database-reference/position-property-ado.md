---
<span data-ttu-id="fdbb1-101"><<<<<<< ヘッド タイトル: 位置プロパティ (ADO) TOCTitle: 位置プロパティ (ADO) === タイトル: Position プロパティ (ADO) TOCTitle: Position プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="fdbb1-101"><<<<<<< HEAD title: Position Property (ADO) TOCTitle: Position Property (ADO) ======= title: Position property (ADO) TOCTitle: Position property (ADO)</span></span>
>>>>>>> <span data-ttu-id="fdbb1-102">マスターの ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID: 48546709 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="fdbb1-102">master ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID: 48546709 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="fdbb1-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="fdbb1-103"><<<<<<< HEAD</span></span>
# <a name="position-property-ado"></a><span data-ttu-id="fdbb1-104">Position プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="fdbb1-104">Position Property (ADO)</span></span>
=======
# <a name="position-property-ado"></a><span data-ttu-id="fdbb1-105">Position プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="fdbb1-105">Position property (ADO)</span></span>
>>>>>>> <span data-ttu-id="fdbb1-106">master</span><span class="sxs-lookup"><span data-stu-id="fdbb1-106">master</span></span>


<span data-ttu-id="fdbb1-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fdbb1-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fdbb1-108">[Stream](stream-object-ado.md) オブジェクト内の現在の位置を示します。</span><span class="sxs-lookup"><span data-stu-id="fdbb1-108">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

<span data-ttu-id="fdbb1-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="fdbb1-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="fdbb1-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="fdbb1-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="fdbb1-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="fdbb1-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="fdbb1-112">master</span><span class="sxs-lookup"><span data-stu-id="fdbb1-112">master</span></span>

<span data-ttu-id="fdbb1-p101">ストリームの先頭から現在位置までのオフセットをバイト単位で示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 0 で、ストリームの最初のバイトを表します。</span><span class="sxs-lookup"><span data-stu-id="fdbb1-p101">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdbb1-115">解説</span><span class="sxs-lookup"><span data-stu-id="fdbb1-115">Remarks</span></span>

<span data-ttu-id="fdbb1-p102">現在位置はストリームの末尾よりも後ろに移動できます。ストリームの末尾を越えて現在位置を指定すると、 [Stream](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) オブジェクトの **Size** も拡張されます。この方法で追加された新しいバイトはすべて Null になります。</span><span class="sxs-lookup"><span data-stu-id="fdbb1-p102">The current position can be moved to a point after the end of the stream. If you specify the current position beyond the end of the stream, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** object will be increased accordingly. Any new bytes added in this way will be null.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fdbb1-p103">[!メモ] <STRONG>Position</STRONG> は常にバイト単位です。マルチバイト文字セットを使用するテキスト ストリームでは、位置と文字サイズを乗算することによって文字数がわかります。たとえば、2 バイト文字セットの場合、最初の文字の位置は 0、2 番目の文字の位置は 2、3 番目の文字の位置は 4 のようになります。</span><span class="sxs-lookup"><span data-stu-id="fdbb1-p103"><STRONG>Position</STRONG> always measures bytes. For text streams using multibyte character sets, multiply the position by the character size to determine the character number. For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span></P>



<span data-ttu-id="fdbb1-p104">負の値を使用して **Stream** 内の現在位置を変更することはできません。 **Position** で使用できるのは正の値だけです。</span><span class="sxs-lookup"><span data-stu-id="fdbb1-p104">Negative values cannot be used to change the current position in a **Stream**. Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="fdbb1-p105">読み取り専用の **Stream** オブジェクトの場合、 **Position** が **Stream** の **Size** よりも大きい値に設定されていても ADO はエラーを返しません。これによって、 **Stream** のサイズや、 **Stream** の内容が変更されることはありません。ただし、 **Position** の値が意味のない値になるので、このような操作はしないでください。</span><span class="sxs-lookup"><span data-stu-id="fdbb1-p105">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**. This does not change the size of the **Stream**, or alter the **Stream** contents in any way. However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>

