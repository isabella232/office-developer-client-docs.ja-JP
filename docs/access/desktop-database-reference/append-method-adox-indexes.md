---
title: Append メソッド (ADOX Indexes)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41eb1cc67dd5a2058f9c5673db381f0bc9067454
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921482"
---
# <a name="append-method-adox-indexes"></a><span data-ttu-id="7f02d-102">Append メソッド (ADOX Indexes)</span><span class="sxs-lookup"><span data-stu-id="7f02d-102">Append method (ADOX Indexes)</span></span>


<span data-ttu-id="7f02d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7f02d-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="7f02d-104">新しい [Index](index-object-adox.md) オブジェクトを [Indexes](indexes-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="7f02d-104">Adds a new [Index](index-object-adox.md) object to the [Indexes](indexes-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f02d-105">構文</span><span class="sxs-lookup"><span data-stu-id="7f02d-105">Syntax</span></span>

<span data-ttu-id="7f02d-106">*インデックス*です。*インデックス*を追加する\[、*列*\]</span><span class="sxs-lookup"><span data-stu-id="7f02d-106">*Indexes*.Append*Index* \[,*Columns*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="7f02d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7f02d-107">Parameters</span></span>

  - <span data-ttu-id="7f02d-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="7f02d-108">*Index*</span></span>

  - <span data-ttu-id="7f02d-109">追加する **Index** オブジェクトを指定します。または、新たに作成して追加するインデックスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f02d-109">The **Index** object to append or the name of the index to create and append.</span></span>

  - <span data-ttu-id="7f02d-110">*Columns*</span><span class="sxs-lookup"><span data-stu-id="7f02d-110">*Columns*</span></span>

  - <span data-ttu-id="7f02d-111">省略可能です。</span><span class="sxs-lookup"><span data-stu-id="7f02d-111">Optional.</span></span> <span data-ttu-id="7f02d-112">インデックスが作成される列の名前を示すバリアント型 ( **Variant** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f02d-112">A **Variant** value that specifies the name(s) of the column(s) to be indexed.</span></span> <span data-ttu-id="7f02d-113">*Columns*パラメーターは、[列](column-object-adox.md)オブジェクトまたはオブジェクトの[Name](name-property-adox.md)プロパティの値に対応します。</span><span class="sxs-lookup"><span data-stu-id="7f02d-113">The *Columns* parameter corresponds to the value(s) of the [Name](name-property-adox.md) property of a [Column](column-object-adox.md) object or objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f02d-114">備考</span><span class="sxs-lookup"><span data-stu-id="7f02d-114">Remarks</span></span>

<span data-ttu-id="7f02d-115">*Columns*パラメーターには、列の名前または列名の配列のいずれかを実行できます。</span><span class="sxs-lookup"><span data-stu-id="7f02d-115">The *Columns* parameter can take either the name of a column or an array of column names.</span></span>

<span data-ttu-id="7f02d-116">プロバイダーがインデックスの作成をサポートしていない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7f02d-116">An error will occur if the provider does not support creating indexes.</span></span>

