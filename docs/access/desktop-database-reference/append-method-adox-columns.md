---
title: Append メソッド (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 727634356a08646b1e2757996cc6bf071de07353
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861576"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="f4a7c-102">Append メソッド (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="f4a7c-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="f4a7c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4a7c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f4a7c-104">新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a7c-105">構文</span><span class="sxs-lookup"><span data-stu-id="f4a7c-105">Syntax</span></span>

<span data-ttu-id="f4a7c-106">*列*です。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-106">*Columns*.</span></span> <span data-ttu-id="f4a7c-107">*列*を追加する\[、*タイプ*\] \[、*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="f4a7c-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="f4a7c-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f4a7c-108">Parameters</span></span>

  - <span data-ttu-id="f4a7c-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="f4a7c-109">*Column*</span></span>

  - <span data-ttu-id="f4a7c-110">追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="f4a7c-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="f4a7c-111">*Type*</span></span>

  - <span data-ttu-id="f4a7c-112">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-112">Optional.</span></span> <span data-ttu-id="f4a7c-113">列のデータ型を指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="f4a7c-114">*型*パラメーターは、**列**オブジェクトの[Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\))プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="f4a7c-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="f4a7c-115">*DefinedSize*</span></span>

  - <span data-ttu-id="f4a7c-116">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-116">Optional.</span></span> <span data-ttu-id="f4a7c-117">列のサイズを指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="f4a7c-118">*DefinedSize*パラメーターは、**列**オブジェクトの[DefinedSize](definedsize-property-adox.md)プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <span data-ttu-id="f4a7c-119">[!メモ] **Column** を **Index** の [Columns](index-object-adox.md) コレクションに追加するときに、 **Tables** コレクションに既に追加されている [Table](table-object-adox.md) にまだ [Column](tables-collection-adox.md) が存在していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f4a7c-119">An error will occur when appending a **Column** to the **Columns** collection of an [Index](index-object-adox.md) if the **Column** does not exist in a [Table](table-object-adox.md) that is already appended to the [Tables](tables-collection-adox.md) collection.</span></span>


