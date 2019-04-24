---
title: Append メソッド (ADOX Keys)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297089"
---
# <a name="append-method-adox-keys"></a><span data-ttu-id="d6566-102">Append メソッド (ADOX Keys)</span><span class="sxs-lookup"><span data-stu-id="d6566-102">Append method (ADOX Keys)</span></span>

<span data-ttu-id="d6566-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6566-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6566-104">新しい [Key](key-object-adox.md) オブジェクトを [Keys](keys-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="d6566-104">Adds a new [Key](key-object-adox.md) object to the [Keys](keys-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6566-105">構文</span><span class="sxs-lookup"><span data-stu-id="d6566-105">Syntax</span></span>

<span data-ttu-id="d6566-106">*キー*。Append*Key* \[、*KeyType* \] \[、\*\* \] Column \[、の各*テーブル*\] \[、および、その他の*列*\]</span><span class="sxs-lookup"><span data-stu-id="d6566-106">*Keys*.Append*Key* \[,*KeyType*\] \[,*Column*\] \[,*RelatedTable*\] \[,*RelatedColumn*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="d6566-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d6566-107">Parameters</span></span>

|<span data-ttu-id="d6566-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d6566-108">Parameter</span></span>|<span data-ttu-id="d6566-109">説明</span><span class="sxs-lookup"><span data-stu-id="d6566-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d6566-110">*Key*</span><span class="sxs-lookup"><span data-stu-id="d6566-110">*Key*</span></span> |<span data-ttu-id="d6566-111">追加する **Key** オブジェクトを指定します。または、作成して追加するキーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="d6566-111">The **Key** object to append or the name of the key to create and append.</span></span>|
|<span data-ttu-id="d6566-112">*KeyType*</span><span class="sxs-lookup"><span data-stu-id="d6566-112">*KeyType*</span></span> |<span data-ttu-id="d6566-113">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="d6566-113">Optional.</span></span> <span data-ttu-id="d6566-114">キーの種類を示す長整数型 (**Long**) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d6566-114">A **Long** value that specifies the type of key.</span></span> <span data-ttu-id="d6566-115">*Key* パラメーターは、**Key** オブジェクトの [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="d6566-115">The *Key* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property of a **Key** object.</span></span>|
|<span data-ttu-id="d6566-116">*列*</span><span class="sxs-lookup"><span data-stu-id="d6566-116">*Column*</span></span> |<span data-ttu-id="d6566-p102">省略可能です。インデックスが作成される列の名前を指定する文字列型 (**String**) の値を指定します。*Columns* パラメーターは、[Column](column-object-adox.md) オブジェクトの [Name](name-property-adox.md) プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="d6566-p102">Optional. A **String** value that specifies the name of the column to be indexed. The *Columns* parameter corresponds to the value of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object.</span></span>|
|<span data-ttu-id="d6566-120">*RelatedTable*</span><span class="sxs-lookup"><span data-stu-id="d6566-120">*RelatedTable*</span></span> |<span data-ttu-id="d6566-p103">省略可能です。リレーション テーブルの名前を示す文字列型 (**String**) の値を指定します。*RelatedTable* パラメーターは、[Table](table-object-adox.md) オブジェクトの **Name** プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="d6566-p103">Optional. A **String** value that specifies the name of the related table. The *RelatedTable* parameter corresponds to the value of the **Name** property of a [Table](table-object-adox.md) object.</span></span>|
|<span data-ttu-id="d6566-124">*RelatedColumn*</span><span class="sxs-lookup"><span data-stu-id="d6566-124">*RelatedColumn*</span></span> |<span data-ttu-id="d6566-p104">省略可能です。外部キーの関連する列の名前を示す文字列型 ( **String** ) の値を指定します。RelatedColumn パラメーターは、 **Column** オブジェクトの **Name** プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="d6566-p104">Optional. A **String** value that specifies the name of the related column for a foreign key. The RelatedColumn parameter corresponds to the value of the **Name** property of a **Column** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d6566-128">注釈</span><span class="sxs-lookup"><span data-stu-id="d6566-128">Remarks</span></span>

<span data-ttu-id="d6566-129">*Columns* パラメーターは、列の名前または列の名前の配列のいずれかとなります。</span><span class="sxs-lookup"><span data-stu-id="d6566-129">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

