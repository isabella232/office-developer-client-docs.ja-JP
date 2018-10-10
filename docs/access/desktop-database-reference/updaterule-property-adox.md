---
title: UpdateRule プロパティ (ADOX)
TOCTitle: UpdateRule Property (ADOX)
ms:assetid: edefa80a-b83b-e811-996c-6f0318722c84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250206(v=office.15)
ms:contentKeyID: 48548548
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a8bdb05dd1c7a16077cfa47c7791b8169c6808aa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479472"
---
# <a name="updaterule-property-adox"></a><span data-ttu-id="67edb-102">UpdateRule プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="67edb-102">UpdateRule Property (ADOX)</span></span>


<span data-ttu-id="67edb-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="67edb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="67edb-104">主キーの更新時に実行されるアクションを示します。</span><span class="sxs-lookup"><span data-stu-id="67edb-104">Indicates the action performed when a primary key is updated.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="67edb-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="67edb-105">Settings and Return Values</span></span>

<span data-ttu-id="67edb-p101">**RuleEnum** 定数の 1 つである長整数型 ( [Long](ruleenum.md) ) の値を設定および取得します。既定値は **adRINone** です。</span><span class="sxs-lookup"><span data-stu-id="67edb-p101">Sets and returns a **Long** value that can be one of the [RuleEnum](ruleenum.md) constants. The default value is **adRINone**.</span></span>

## <a name="remarks"></a><span data-ttu-id="67edb-108">解説</span><span class="sxs-lookup"><span data-stu-id="67edb-108">Remarks</span></span>

<span data-ttu-id="67edb-109">このプロパティは、[Key](key-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="67edb-109">This property is read-only on [Key](key-object-adox.md) objects already appended to the collection.</span></span>

