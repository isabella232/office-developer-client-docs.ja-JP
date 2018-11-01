---
title: LineSeparator プロパティ (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 831b6377ade43b3be04ed21add20fbd10e48ac2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882505"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="ad84b-102">LineSeparator プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="ad84b-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="ad84b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ad84b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad84b-104">テキスト [Stream](stream-object-ado.md) オブジェクトの行区切り文字として使用するバイナリ文字を示します。</span><span class="sxs-lookup"><span data-stu-id="ad84b-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ad84b-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="ad84b-105">Settings and return values</span></span>

<span data-ttu-id="ad84b-p101">[Stream](lineseparatorsenum.md) で使う行区切り文字を示す **LineSeparatorsEnum** 値を設定または取得します。既定値は **adCRLF** です。</span><span class="sxs-lookup"><span data-stu-id="ad84b-p101">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**. The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad84b-108">解説</span><span class="sxs-lookup"><span data-stu-id="ad84b-108">Remarks</span></span>

<span data-ttu-id="ad84b-p102">**LineSeparator** は、テキスト **Stream** の内容を読むときに行を解釈するために使います。行は、 [SkipLine](skipline-method-ado.md) メソッドで読み飛ばすこともできます。</span><span class="sxs-lookup"><span data-stu-id="ad84b-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="ad84b-p103">**LineSeparator** は、テキスト **Stream** オブジェクト ([Type](type-property-ado-stream.md) が **adTypeText**) だけに使用します。**Type** が **adTypeBinary** の場合、このプロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="ad84b-p103">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

