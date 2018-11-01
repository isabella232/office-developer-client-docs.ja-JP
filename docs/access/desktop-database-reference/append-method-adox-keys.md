---
title: Append メソッド (ADOX Keys)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5ba46c922ff9fc27da0abc1908f6ffaff8e997ef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879460"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="4a2f0-102">Append メソッド (ADOX Keys)</span><span class="sxs-lookup"><span data-stu-id="4a2f0-102">Append Method (ADOX Keys)</span></span>


<span data-ttu-id="4a2f0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="4a2f0-104">新しい [Key](key-object-adox.md) オブジェクトを [Keys](keys-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2f0-105">構文</span><span class="sxs-lookup"><span data-stu-id="4a2f0-105">Syntax</span></span>

<span data-ttu-id="4a2f0-106">*キー*。*キー*を追加する\[、*KeyType* \] \[、*列*\] \[、*RelatedTable* \] \[、*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="4a2f0-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="4a2f0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4a2f0-107">Parameters</span></span>

  - <span data-ttu-id="4a2f0-108">*Key*</span><span class="sxs-lookup"><span data-stu-id="4a2f0-108">*Key*</span></span>

  - <span data-ttu-id="4a2f0-109">追加する **Key** オブジェクトを指定します。または、作成して追加するキーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-109">The **Key** object to append or the name of the key to create and append.</span></span>

  - <span data-ttu-id="4a2f0-110">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="4a2f0-110">*KeyType*</span></span>

  - <span data-ttu-id="4a2f0-111">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-111">Optional.</span></span> <span data-ttu-id="4a2f0-112">キーの種類を示す長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-112">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="4a2f0-113">*Key*パラメーターは、**キー**オブジェクトの[Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\))プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-113">The *Key* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property of a **Key** object.</span></span>

  - <span data-ttu-id="4a2f0-114">*Column*</span><span class="sxs-lookup"><span data-stu-id="4a2f0-114">*Column*</span></span>

  - <span data-ttu-id="4a2f0-115">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-115">Optional.</span></span> <span data-ttu-id="4a2f0-116">インデックスが作成される列の名前を指定する文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-116">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="4a2f0-117">*Columns*パラメーターは、 [Column](column-object-adox.md)オブジェクトの[Name](name-property-adox.md)プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-117">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>

  - <span data-ttu-id="4a2f0-118">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="4a2f0-118">*RelatedTable*</span></span>

  - <span data-ttu-id="4a2f0-119">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-119">Optional.</span></span> <span data-ttu-id="4a2f0-120">リレーション テーブルの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-120">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="4a2f0-121">*RelatedTable*パラメーターは、[テーブル](table-object-adox.md)オブジェクトの**Name**プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-121">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>

  - <span data-ttu-id="4a2f0-122">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="4a2f0-122">*RelatedColumn*</span></span>

  - <span data-ttu-id="4a2f0-p104">省略可能です。外部キーの関連する列の名前を示す文字列型 ( **String** ) の値を指定します。RelatedColumn パラメーターは、 **Column** オブジェクトの **Name** プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a2f0-126">解説</span><span class="sxs-lookup"><span data-stu-id="4a2f0-126">Remarks</span></span>

<span data-ttu-id="4a2f0-127">*Columns*パラメーターには、列の名前または列名の配列のいずれかを実行できます。</span><span class="sxs-lookup"><span data-stu-id="4a2f0-127">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

