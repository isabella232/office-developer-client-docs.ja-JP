---
title: Append メソッド (ADOX Keys)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d99af00f1ad83087994737f5bb3ca29acf2a9deb
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949818"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="35c50-102">Append メソッド (ADOX Keys)</span><span class="sxs-lookup"><span data-stu-id="35c50-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="35c50-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="35c50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35c50-104">新しい [Key](key-object-adox.md) オブジェクトを [Keys](keys-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="35c50-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c50-105">構文</span><span class="sxs-lookup"><span data-stu-id="35c50-105">Syntax</span></span>

<span data-ttu-id="35c50-106">*キー*。*キー*を追加する\[、*KeyType* \] \[、*列*\] \[、*RelatedTable* \] \[、*RelatedColumn*\]</span><span class="sxs-lookup"><span data-stu-id="35c50-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="35c50-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35c50-107">Parameters</span></span>

|<span data-ttu-id="35c50-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35c50-108">Parameter</span></span>|<span data-ttu-id="35c50-109">説明</span><span class="sxs-lookup"><span data-stu-id="35c50-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="35c50-110">*Key*</span><span class="sxs-lookup"><span data-stu-id="35c50-110">*Key*</span></span> |<span data-ttu-id="35c50-111">追加する **Key** オブジェクトを指定します。または、作成して追加するキーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="35c50-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="35c50-112">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="35c50-112">*KeyType*</span></span> |<span data-ttu-id="35c50-113">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="35c50-113">Optional.</span></span> <span data-ttu-id="35c50-114">キーの種類を示す長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="35c50-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="35c50-115">*Key*パラメーターは、**キー**オブジェクトの[Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="35c50-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="35c50-116">*Column*</span><span class="sxs-lookup"><span data-stu-id="35c50-116">*Column*</span></span> |<span data-ttu-id="35c50-117">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="35c50-117">Optional.</span></span> <span data-ttu-id="35c50-118">インデックスが作成される列の名前を指定する文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="35c50-118">A **String** value that specifies the name of the column to be indexed.</span></span> <span data-ttu-id="35c50-119">*Columns*パラメーターは、 [Column](column-object-adox.md)オブジェクトの[Name](name-property-adox.md)プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="35c50-119">The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="35c50-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="35c50-120">*RelatedTable*</span></span> |<span data-ttu-id="35c50-121">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="35c50-121">Optional.</span></span> <span data-ttu-id="35c50-122">リレーション テーブルの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="35c50-122">A **String** value that specifies the name of the related table.</span></span> <span data-ttu-id="35c50-123">*RelatedTable*パラメーターは、[テーブル](table-object-adox.md)オブジェクトの**Name**プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="35c50-123">The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="35c50-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="35c50-124">*RelatedColumn*</span></span> |<span data-ttu-id="35c50-p104">省略可能です。外部キーの関連する列の名前を示す文字列型 ( **String** ) の値を指定します。RelatedColumn パラメーターは、 **Column** オブジェクトの **Name** プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="35c50-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="35c50-128">解説</span><span class="sxs-lookup"><span data-stu-id="35c50-128">Remarks</span></span>

<span data-ttu-id="35c50-129">*Columns*パラメーターには、列の名前または列名の配列のいずれかを実行できます。</span><span class="sxs-lookup"><span data-stu-id="35c50-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

