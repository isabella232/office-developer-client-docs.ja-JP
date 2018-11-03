---
title: UpdateRule プロパティ (ADOX)
TOCTitle: UpdateRule property (ADOX)
ms:assetid: edefa80a-b83b-e811-996c-6f0318722c84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250206(v=office.15)
ms:contentKeyID: 48548548
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a1900ab0fffbad44547d2cc0a3cde856633f8624
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923400"
---
# <a name="updaterule-property-adox"></a><span data-ttu-id="1a6ab-102">UpdateRule プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="1a6ab-102">UpdateRule property (ADOX)</span></span>


<span data-ttu-id="1a6ab-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1a6ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a6ab-104">主キーの更新時に実行されるアクションを示します。</span><span class="sxs-lookup"><span data-stu-id="1a6ab-104">Indicates the action performed when a primary key is updated.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1a6ab-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="1a6ab-105">Settings and return values</span></span>

<span data-ttu-id="1a6ab-p101">**RuleEnum** 定数の 1 つである長整数型 ( [Long](ruleenum.md) ) の値を設定および取得します。既定値は **adRINone** です。</span><span class="sxs-lookup"><span data-stu-id="1a6ab-p101">Sets and returns a **Long** value that can be one of the [RuleEnum](ruleenum.md) constants. The default value is **adRINone**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a6ab-108">解説</span><span class="sxs-lookup"><span data-stu-id="1a6ab-108">Remarks</span></span>

<span data-ttu-id="1a6ab-109">このプロパティは、[Key](key-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="1a6ab-109">This property is read-only on [Key](key-object-adox.md) objects already appended to the collection.</span></span>

