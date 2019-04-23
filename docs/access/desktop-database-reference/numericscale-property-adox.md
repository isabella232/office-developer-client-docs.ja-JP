---
title: numericscale プロパティ (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288519"
---
# <a name="numericscale-property-adox"></a><span data-ttu-id="2d0db-102">numericscale プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2d0db-102">NumericScale property (ADOX)</span></span>


<span data-ttu-id="2d0db-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d0db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d0db-104">列中の数値の小数点以下の桁数を示します。</span><span class="sxs-lookup"><span data-stu-id="2d0db-104">Indicates the scale of a numeric value in the column.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="2d0db-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="2d0db-105">Settings and return values</span></span>

<span data-ttu-id="2d0db-p101">**Type** プロパティが [adNumeric](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) または **adDecimal** の場合、列にあるデータ値の小数点以下の桁数をバイト型 ( **Byte** ) の値で設定および取得します。その他のすべてのデータ型では、 **NumericScale** は無視されます。</span><span class="sxs-lookup"><span data-stu-id="2d0db-p101">Sets and returns a **Byte** value that is the scale of data values in the column when the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property is **adNumeric** or **adDecimal**. **NumericScale** is ignored for all other data types.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d0db-108">注釈</span><span class="sxs-lookup"><span data-stu-id="2d0db-108">Remarks</span></span>

<span data-ttu-id="2d0db-109">既定値は 0 (ゼロ) です。</span><span class="sxs-lookup"><span data-stu-id="2d0db-109">The default value is zero (0).</span></span>

<span data-ttu-id="2d0db-110">**NumericScale** は、 [Column](column-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="2d0db-110">**NumericScale** is read-only for [Column](column-object-adox.md) objects already appended to a collection.</span></span>

