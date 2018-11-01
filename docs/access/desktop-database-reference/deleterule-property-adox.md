---
title: DeleteRule プロパティ (ADOX)
TOCTitle: DeleteRule Property (ADOX)
ms:assetid: cd05e024-c1fc-a0b8-8ada-e05ec899c334
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250018(v=office.15)
ms:contentKeyID: 48547752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bcc83bc841360407762025206d0f41a21eccd1a4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884171"
---
# <a name="deleterule-property-adox"></a><span data-ttu-id="cfb4c-102">DeleteRule プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cfb4c-102">DeleteRule Property (ADOX)</span></span>


<span data-ttu-id="cfb4c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cfb4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfb4c-104">主キーが削除されたときに実行されるアクションを示します。</span><span class="sxs-lookup"><span data-stu-id="cfb4c-104">Indicates the action performed when a primary key is deleted.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cfb4c-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="cfb4c-105">Settings and return values</span></span>

<span data-ttu-id="cfb4c-p101">**RuleEnum** 定数の 1 つである長整数型 ( [Long](ruleenum.md) ) の値を設定および取得します。既定値は **adRINone** です。</span><span class="sxs-lookup"><span data-stu-id="cfb4c-p101">Sets and returns a **Long** value that can be one of the [RuleEnum](ruleenum.md) constants. The default value is **adRINone**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb4c-108">解説</span><span class="sxs-lookup"><span data-stu-id="cfb4c-108">Remarks</span></span>

<span data-ttu-id="cfb4c-109">このプロパティは、[Key](key-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="cfb4c-109">This property is read-only on [Key](key-object-adox.md) objects already appended to a collection.</span></span>

