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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313581"
---
# <a name="updaterule-property-adox"></a><span data-ttu-id="7b365-102">UpdateRule プロパティ (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7b365-102">UpdateRule property (ADOX)</span></span>


<span data-ttu-id="7b365-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b365-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b365-104">主キーの更新時に実行されるアクションを示します。</span><span class="sxs-lookup"><span data-stu-id="7b365-104">Indicates the action performed when a primary key is updated.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7b365-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="7b365-105">Settings and return values</span></span>

<span data-ttu-id="7b365-106">**RuleEnum** 定数の 1 つである長整数型 ( [Long](ruleenum.md) ) の値を設定および取得します。</span><span class="sxs-lookup"><span data-stu-id="7b365-106">Sets and returns a **Long** value that can be one of the [RuleEnum](ruleenum.md) constants.</span></span> <span data-ttu-id="7b365-107">既定値は **adRINone** です。</span><span class="sxs-lookup"><span data-stu-id="7b365-107">The default value is **adRINone**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b365-108">注釈</span><span class="sxs-lookup"><span data-stu-id="7b365-108">Remarks</span></span>

<span data-ttu-id="7b365-109">このプロパティは、[Key](key-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。</span><span class="sxs-lookup"><span data-stu-id="7b365-109">This property is read-only on [Key](key-object-adox.md) objects already appended to the collection.</span></span>

