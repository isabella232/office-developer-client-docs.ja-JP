---
title: UpdateRule プロパティ (ADOX)
TOCTitle: UpdateRule property (ADOX)
ms:assetid: edefa80a-b83b-e811-996c-6f0318722c84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250206(v=office.15)
ms:contentKeyID: 48548548
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c375a4eb9931008ea9753181b44aa5509377d11
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726233"
---
# <a name="updaterule-property-adox"></a><span data-ttu-id="00cae-102">UpdateRule プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="00cae-102">UpdateRule property (ADOX)</span></span>


<span data-ttu-id="00cae-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="00cae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00cae-104">主キーの更新時に実行されるアクションを示します。</span><span class="sxs-lookup"><span data-stu-id="00cae-104">Indicates the action performed when a primary key is updated.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="00cae-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="00cae-105">Settings and return values</span></span>

<span data-ttu-id="00cae-p101">**RuleEnum** 定数の 1 つである長整数型 ( [Long](ruleenum.md) ) の値を設定および取得します。既定値は **adRINone** です。</span><span class="sxs-lookup"><span data-stu-id="00cae-p101">Sets and returns a **Long** value that can be one of the [RuleEnum](ruleenum.md) constants. The default value is **adRINone**.</span></span>

## <a name="remarks"></a><span data-ttu-id="00cae-108">解説</span><span class="sxs-lookup"><span data-stu-id="00cae-108">Remarks</span></span>

<span data-ttu-id="00cae-109">このプロパティは、[Key](key-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="00cae-109">This property is read-only on [Key](key-object-adox.md) objects already appended to the collection.</span></span>

