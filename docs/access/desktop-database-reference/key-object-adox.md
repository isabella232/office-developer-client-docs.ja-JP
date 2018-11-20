---
title: Key オブジェクト (ADOX のデスクトップのデータベース参照のアクセス)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7722130c76516eaa7dcaf0598a5e1c040e21ba25
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025946"
---
# <a name="key-object-adox"></a><span data-ttu-id="4735c-102">Key オブジェクト (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4735c-102">Key object (ADOX)</span></span>


<span data-ttu-id="4735c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4735c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4735c-104">データベース テーブルの主キー フィールド、外部キー フィールド、または一意なキー フィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="4735c-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="4735c-105">解説</span><span class="sxs-lookup"><span data-stu-id="4735c-105">Remarks</span></span>

<span data-ttu-id="4735c-106">次のコードによって、新しい **Key** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4735c-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="4735c-107">**Key** オブジェクトのプロパティとコレクションを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="4735c-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="4735c-108">[Name](name-property-adox.md) プロパティを使用して、キーを識別します。</span><span class="sxs-lookup"><span data-stu-id="4735c-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="4735c-109">[Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) プロパティを使用して、キーが主キー、外部キー、または一意キーのどれであるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4735c-109">Determine whether the key is primary, foreign, or unique with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property.</span></span>

- <span data-ttu-id="4735c-110">[Columns](columns-collection-adox.md) コレクションを使用して、キーによって指定されたデータベースの列にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4735c-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="4735c-111">[RelatedTable](relatedtable-property-adox.md) プロパティを使用して、関連テーブルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4735c-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="4735c-112">[DeleteRule](deleterule-property-adox.md) プロパティと [UpdateRule](updaterule-property-adox.md) プロパティを使用して、主キーが削除または更新された場合のアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="4735c-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

