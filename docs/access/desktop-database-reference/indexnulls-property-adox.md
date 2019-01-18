---
title: IndexNulls プロパティ (ADOX)
TOCTitle: IndexNulls property (ADOX)
ms:assetid: 5c78c818-c23d-5b2c-d246-531aedc639df
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249326(v=office.15)
ms:contentKeyID: 48545089
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1419abb5dc66a59594284cf319487ef980bf62f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712884"
---
# <a name="indexnulls-property-adox"></a><span data-ttu-id="e7406-102">IndexNulls プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e7406-102">IndexNulls property (ADOX)</span></span>


<span data-ttu-id="e7406-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e7406-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7406-104">インデックス フィールドの Null 値を持つレコードがインデックスへのエントリを持つかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e7406-104">Indicates whether records that have null values in their index fields have index entries.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e7406-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="e7406-105">Settings and return values</span></span>

<span data-ttu-id="e7406-p101">[AllowNullsEnum](allownullsenum.md) 値を設定および取得します。既定値は **adIndexNullsDisallow** です。</span><span class="sxs-lookup"><span data-stu-id="e7406-p101">Sets and returns an [AllowNullsEnum](allownullsenum.md) value. The default value is **adIndexNullsDisallow**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7406-108">解説</span><span class="sxs-lookup"><span data-stu-id="e7406-108">Remarks</span></span>

<span data-ttu-id="e7406-109">このプロパティは、[Index](index-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="e7406-109">This property is read-only on [Index](index-object-adox.md) objects already appended to a collection.</span></span>

