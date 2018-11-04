---
title: Append メソッド (ADOX Columns)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7a6f7ac26c3089a973a68e07acbe0f6f3e4029df
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949440"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="49ef8-102">Append メソッド (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="49ef8-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="49ef8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="49ef8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49ef8-104">新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="49ef8-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ef8-105">構文</span><span class="sxs-lookup"><span data-stu-id="49ef8-105">Syntax</span></span>

<span data-ttu-id="49ef8-106">*列*です。</span><span class="sxs-lookup"><span data-stu-id="49ef8-106">*Columns*.</span></span> <span data-ttu-id="49ef8-107">*列*を追加する\[、*タイプ*\] \[、*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="49ef8-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="49ef8-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49ef8-108">Parameters</span></span>

|<span data-ttu-id="49ef8-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49ef8-109">Parameter</span></span>|<span data-ttu-id="49ef8-110">説明</span><span class="sxs-lookup"><span data-stu-id="49ef8-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="49ef8-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="49ef8-111">*Column*</span></span> |<span data-ttu-id="49ef8-112">追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="49ef8-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="49ef8-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="49ef8-113">*Type*</span></span> |<span data-ttu-id="49ef8-114">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="49ef8-114">Optional.</span></span> <span data-ttu-id="49ef8-115">列のデータ型を指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="49ef8-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="49ef8-116">*型*パラメーターは、**列**オブジェクトの[Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\))プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="49ef8-116">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>|
|<span data-ttu-id="49ef8-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="49ef8-117">*DefinedSize*</span></span> |<span data-ttu-id="49ef8-118">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="49ef8-118">Optional.</span></span> <span data-ttu-id="49ef8-119">列のサイズを指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="49ef8-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="49ef8-120">*DefinedSize*パラメーターは、**列**オブジェクトの[DefinedSize](definedsize-property-adox.md)プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="49ef8-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="49ef8-121">[!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="49ef8-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


