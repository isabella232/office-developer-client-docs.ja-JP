---
title: NumericScale プロパティ (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11696e379fe618f07a6087eee26ba21a2d27b3e5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890919"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="36490-102">NumericScale プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="36490-102">NumericScale Property (ADOX)</span></span>


<span data-ttu-id="36490-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="36490-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36490-104">列中の数値の小数点以下の桁数を示します。</span><span class="sxs-lookup"><span data-stu-id="36490-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="36490-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="36490-105">Settings and return values</span></span>

<span data-ttu-id="36490-p101">**Type** プロパティが [adNumeric](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) または **adDecimal** の場合、列にあるデータ値の小数点以下の桁数をバイト型 ( **Byte** ) の値で設定および取得します。その他のすべてのデータ型では、 **NumericScale** は無視されます。</span><span class="sxs-lookup"><span data-stu-id="36490-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="36490-108">解説</span><span class="sxs-lookup"><span data-stu-id="36490-108">Remarks</span></span>

<span data-ttu-id="36490-109">既定値は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="36490-109">The default value is zero (0).</span></span>

<span data-ttu-id="36490-110">**NumericScale** は、 [Column](column-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="36490-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

