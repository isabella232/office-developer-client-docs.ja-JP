---
title: Key オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11bd05c4959ba1f3e1819e482ce311fc798bf0e6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929833"
---
# <a name="key-object-adox"></a><span data-ttu-id="6237e-102">Key オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="6237e-102">Key object (ADOX)</span></span>


<span data-ttu-id="6237e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6237e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6237e-104">データベース テーブルの主キー フィールド、外部キー フィールド、または一意なキー フィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="6237e-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="6237e-105">解説</span><span class="sxs-lookup"><span data-stu-id="6237e-105">Remarks</span></span>

<span data-ttu-id="6237e-106">次のコードによって、新しい **Key** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="6237e-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="6237e-107">**Key** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6237e-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="6237e-108">[Name](name-property-adox.md) プロパティを使用して、キーを識別します。</span><span class="sxs-lookup"><span data-stu-id="6237e-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="6237e-109">[Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) プロパティを使用して、キーが主キー、外部キー、または一意キーのどれであるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="6237e-109">Determine whether the key is primary, foreign, or unique with the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property.</span></span>

- <span data-ttu-id="6237e-110">[Columns](columns-collection-adox.md) コレクションを使用して、キーによって指定されたデータベースの列にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6237e-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="6237e-111">[RelatedTable](relatedtable-property-adox.md) プロパティを使用して、関連テーブルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6237e-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="6237e-112">[DeleteRule](deleterule-property-adox.md) プロパティと [UpdateRule](updaterule-property-adox.md) プロパティを使用して、主キーが削除または更新された場合のアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="6237e-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

