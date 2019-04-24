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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291477"
---
# <a name="indexnulls-property-adox"></a><span data-ttu-id="04912-102">IndexNulls プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="04912-102">IndexNulls property (ADOX)</span></span>


<span data-ttu-id="04912-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="04912-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04912-104">インデックス フィールドの Null 値を持つレコードがインデックスへのエントリを持つかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="04912-104">Indicates whether records that have null values in their index fields have index entries.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="04912-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="04912-105">Settings and return values</span></span>

<span data-ttu-id="04912-106">[AllowNullsEnum](allownullsenum.md) 値を設定および取得します。</span><span class="sxs-lookup"><span data-stu-id="04912-106">Sets and returns an [AllowNullsEnum](allownullsenum.md) value.</span></span> <span data-ttu-id="04912-107">既定値は **adIndexNullsDisallow** です。</span><span class="sxs-lookup"><span data-stu-id="04912-107">The default value is **adIndexNullsDisallow**.</span></span>

## <a name="remarks"></a><span data-ttu-id="04912-108">注釈</span><span class="sxs-lookup"><span data-stu-id="04912-108">Remarks</span></span>

<span data-ttu-id="04912-109">このプロパティは、[Index](index-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="04912-109">This property is read-only on [Index](index-object-adox.md) objects already appended to a collection.</span></span>

