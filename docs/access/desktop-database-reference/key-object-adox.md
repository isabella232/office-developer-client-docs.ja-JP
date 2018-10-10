---
title: Key オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c77e45f52994f14d79acf424da14b55b2cdd9814
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479714"
---
# <a name="key-object-adox"></a><span data-ttu-id="21278-102">Key オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="21278-102">Key Object (ADOX)</span></span>


<span data-ttu-id="21278-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="21278-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="21278-104">データベース テーブルの主キー フィールド、外部キー フィールド、または一意なキー フィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="21278-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="21278-105">解説</span><span class="sxs-lookup"><span data-stu-id="21278-105">Remarks</span></span>

<span data-ttu-id="21278-106">次のコードによって、新しい **Key** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="21278-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="21278-107">**Key** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="21278-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="21278-108">[Name](name-property-adox.md) プロパティを使用して、キーを識別します。</span><span class="sxs-lookup"><span data-stu-id="21278-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="21278-109">[Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) プロパティを使用して、キーが主キー、外部キー、または一意キーのどれであるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="21278-109">Determine whether the key is primary, foreign, or unique with the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property.</span></span>

- <span data-ttu-id="21278-110">[Columns](columns-collection-adox.md) コレクションを使用して、キーによって指定されたデータベースの列にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="21278-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="21278-111">[RelatedTable](relatedtable-property-adox.md) プロパティを使用して、関連テーブルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="21278-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="21278-112">[DeleteRule](deleterule-property-adox.md) プロパティと [UpdateRule](updaterule-property-adox.md) プロパティを使用して、主キーが削除または更新された場合のアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="21278-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

