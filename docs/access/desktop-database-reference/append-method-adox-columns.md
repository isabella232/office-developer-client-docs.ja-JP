---
title: Append メソッド (ADOX Columns)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 12e79802587874aacb5b47a56387e331b8148069
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026373"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="bd963-102">Append メソッド (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="bd963-102">Append method (ADOX Columns)</span></span>

<span data-ttu-id="bd963-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bd963-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd963-104">新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bd963-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd963-105">構文</span><span class="sxs-lookup"><span data-stu-id="bd963-105">Syntax</span></span>

<span data-ttu-id="bd963-106">*列*です。</span><span class="sxs-lookup"><span data-stu-id="bd963-106">*Columns*.</span></span> <span data-ttu-id="bd963-107">*列*を追加する\[、*タイプ*\] \[、*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="bd963-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="bd963-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="bd963-108">Parameters</span></span>

|<span data-ttu-id="bd963-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bd963-109">Parameter</span></span>|<span data-ttu-id="bd963-110">説明</span><span class="sxs-lookup"><span data-stu-id="bd963-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="bd963-111">*Column*</span><span class="sxs-lookup"><span data-stu-id="bd963-111">*Column*</span></span> |<span data-ttu-id="bd963-112">追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd963-112">The **Column** object to append or the name of the column to create and append.</span></span>|
|<span data-ttu-id="bd963-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="bd963-113">*Type*</span></span> |<span data-ttu-id="bd963-114">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="bd963-114">Optional.</span></span> <span data-ttu-id="bd963-115">列のデータ型を指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd963-115">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="bd963-116">*型*パラメーターは、**列**オブジェクトの[Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="bd963-116">The *Type* parameter corresponds to the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property of a **Column** object.</span></span>|
|<span data-ttu-id="bd963-117">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="bd963-117">*DefinedSize*</span></span> |<span data-ttu-id="bd963-118">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="bd963-118">Optional.</span></span> <span data-ttu-id="bd963-119">列のサイズを指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bd963-119">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="bd963-120">*DefinedSize*パラメーターは、**列**オブジェクトの[DefinedSize](definedsize-property-adox.md)プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="bd963-120">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>|


> [!NOTE]
> <span data-ttu-id="bd963-121">[!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bd963-121">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


