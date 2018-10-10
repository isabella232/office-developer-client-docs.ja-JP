---
title: NumericScale プロパティ (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4229a318c4eb855b86164f02f1075d29a915d718
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478453"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="a024f-102">NumericScale プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a024f-102">NumericScale Property (ADOX)</span></span>


<span data-ttu-id="a024f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a024f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a024f-104">列中の数値の小数点以下の桁数を示します。</span><span class="sxs-lookup"><span data-stu-id="a024f-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a024f-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="a024f-105">Settings and Return Values</span></span>

<span data-ttu-id="a024f-p101">**Type** プロパティが [adNumeric](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) または **adDecimal** の場合、列にあるデータ値の小数点以下の桁数をバイト型 ( **Byte** ) の値で設定および取得します。その他のすべてのデータ型では、 **NumericScale** は無視されます。</span><span class="sxs-lookup"><span data-stu-id="a024f-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="a024f-108">解説</span><span class="sxs-lookup"><span data-stu-id="a024f-108">Remarks</span></span>

<span data-ttu-id="a024f-109">既定値は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="a024f-109">The default value is zero (0).</span></span>

<span data-ttu-id="a024f-110">**NumericScale** は、 [Column](column-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="a024f-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

