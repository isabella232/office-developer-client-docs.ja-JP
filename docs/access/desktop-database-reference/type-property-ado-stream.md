---
title: Type プロパティ (ADO Stream)
TOCTitle: Type Property (ADO Stream)
ms:assetid: 43872c74-51bf-47ae-6bdc-55d25b0dc84a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249203(v=office.15)
ms:contentKeyID: 48544505
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2fdf3f40565f41a3d34b2202c4e079839af1f1ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602742"
---
# <a name="type-property-ado-stream"></a><span data-ttu-id="12437-102">Type プロパティ (ADO Stream)</span><span class="sxs-lookup"><span data-stu-id="12437-102">Type Property (ADO Stream)</span></span>


<span data-ttu-id="12437-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="12437-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="12437-104">[Stream](stream-object-ado.md) (バイナリまたはテキスト) に格納されているデータの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="12437-104">Indicates the type of data contained in the [Stream](stream-object-ado.md) (binary or text).</span></span>

<span data-ttu-id="12437-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="12437-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="12437-106">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="12437-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="12437-107">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="12437-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="12437-108">master</span><span class="sxs-lookup"><span data-stu-id="12437-108">master</span></span>

<span data-ttu-id="12437-p101">[Stream](streamtypeenum.md) オブジェクトに格納されたデータの種類を示す **StreamTypeEnum** 値を設定または取得します。既定値は **adTypeText** です。ただし、バイナリ データが新しい空の **Stream** に書き込まれる場合、 **Type** は **adTypeBinary** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="12437-p101">Sets or returns a [StreamTypeEnum](streamtypeenum.md) value that specifies the type of data contained in the **Stream** object. The default value is **adTypeText**. However, if binary data is initially written to a new, empty **Stream**, the **Type** will be changed to **adTypeBinary**.</span></span>

## <a name="remarks"></a><span data-ttu-id="12437-112">解説</span><span class="sxs-lookup"><span data-stu-id="12437-112">Remarks</span></span>

<span data-ttu-id="12437-113">**Type** プロパティは、現在の位置が **Stream** の先頭 ([Position](position-property-ado.md) が 0) である場合にのみ値の取得および設定が可能であり、その他の位置である場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="12437-113">The **Type** property is read/write only when the current position is at the beginning of the **Stream** ([Position](position-property-ado.md) is 0), and read-only at any other position.</span></span>

<span data-ttu-id="12437-p102">**Type** プロパティによって、 **Stream** の読み取りと書き込みに使用するメソッドが決まります。テキスト **Stream** の場合は、 [ReadText](readtext-method-ado.md) および [WriteText](writetext-method-ado.md) を使用します。バイナリ **Stream** の場合は、 [Read](read-method-ado.md) および [Write](write-method-ado.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="12437-p102">The **Type** property determines which methods should be used for reading and writing the **Stream**. For text **Streams**, use [ReadText](readtext-method-ado.md) and [WriteText](writetext-method-ado.md). For binary **Streams**, use [Read](read-method-ado.md) and [Write](write-method-ado.md).</span></span>

