---
title: Append メソッド (ADOX Columns)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476675"
---
# <a name="append-method-adox-columns"></a><span data-ttu-id="befca-102">Append メソッド (ADOX Columns)</span><span class="sxs-lookup"><span data-stu-id="befca-102">Append Method (ADOX Columns)</span></span>


<span data-ttu-id="befca-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="befca-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="befca-104">新しい [Column](column-object-adox.md) オブジェクトを [Columns](columns-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="befca-104">Adds a new [Column](column-object-adox.md) object to the [Columns](columns-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="befca-105">構文</span><span class="sxs-lookup"><span data-stu-id="befca-105">Syntax</span></span>

<span data-ttu-id="befca-106">*列*です。</span><span class="sxs-lookup"><span data-stu-id="befca-106">*Columns*.</span></span> <span data-ttu-id="befca-107">*列*を追加する\[、*タイプ*\] \[、*DefinedSize*\]</span><span class="sxs-lookup"><span data-stu-id="befca-107">Append*Column* \[,*Type*\] \[,*DefinedSize*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="befca-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="befca-108">Parameters</span></span>

  - <span data-ttu-id="befca-109">*Column*</span><span class="sxs-lookup"><span data-stu-id="befca-109">*Column*</span></span>

  - <span data-ttu-id="befca-110">追加する **Column** オブジェクトを指定します。または、新たに作成して追加する列の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="befca-110">The **Column** object to append or the name of the column to create and append.</span></span>

  - <span data-ttu-id="befca-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="befca-111">*Type*</span></span>

  - <span data-ttu-id="befca-112">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="befca-112">Optional.</span></span> <span data-ttu-id="befca-113">列のデータ型を指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="befca-113">A **Long** value that specifies the data type of the column.</span></span> <span data-ttu-id="befca-114">*型*パラメーターは、**列**オブジェクトの[Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\))プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="befca-114">The *Type* parameter corresponds to the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property of a **Column** object.</span></span>

  - <span data-ttu-id="befca-115">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="befca-115">*DefinedSize*</span></span>

  - <span data-ttu-id="befca-116">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="befca-116">Optional.</span></span> <span data-ttu-id="befca-117">列のサイズを指定する長整数型 ( **Long** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="befca-117">A **Long** value that specifies the size of the column.</span></span> <span data-ttu-id="befca-118">*DefinedSize*パラメーターは、**列**オブジェクトの[DefinedSize](definedsize-property-adox.md)プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="befca-118">The *DefinedSize* parameter corresponds to the [DefinedSize](definedsize-property-adox.md) property of a **Column** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="befca-119">[!メモ] <STRONG>Column</STRONG> を <STRONG>Index</STRONG> の <A href="index-object-adox.md">Columns</A> コレクションに追加するときに、 <STRONG>Tables</STRONG> コレクションに既に追加されている <A href="table-object-adox.md">Table</A> にまだ <A href="tables-collection-adox.md">Column</A> が存在していない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="befca-119">An error will occur when appending a <STRONG>Column</STRONG> to the <STRONG>Columns</STRONG> collection of an <A href="index-object-adox.md">Index</A> if the <STRONG>Column</STRONG> does not exist in a <A href="table-object-adox.md">Table</A> that is already appended to the <A href="tables-collection-adox.md">Tables</A> collection.</span></span></P>


