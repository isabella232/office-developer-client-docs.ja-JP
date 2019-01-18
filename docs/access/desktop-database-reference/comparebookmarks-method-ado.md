---
title: CompareBookmarks メソッド (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 460a77284141daad1834699c4dc1775be05c5c26
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712163"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="81780-102">CompareBookmarks メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="81780-102">CompareBookmarks method (ADO)</span></span>

<span data-ttu-id="81780-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="81780-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81780-104">2 つのブックマークを比較して、相対的な位置を示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="81780-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="81780-105">構文</span><span class="sxs-lookup"><span data-stu-id="81780-105">Syntax</span></span>

<span data-ttu-id="81780-106">*結果* = *レコード セット*です。CompareBookmarks (*Bookmark1*、 *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="81780-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="81780-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="81780-107">Return value</span></span>

<span data-ttu-id="81780-108">ブックマークで表される 2 つのレコードの相対的な行位置を示す [CompareEnum](compareenum.md) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="81780-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="81780-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81780-109">Parameters</span></span>

|<span data-ttu-id="81780-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="81780-110">Parameter</span></span>|<span data-ttu-id="81780-111">説明</span><span class="sxs-lookup"><span data-stu-id="81780-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="81780-112">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="81780-112">*Bookmark1*</span></span> |<span data-ttu-id="81780-113">最初の行のブックマークです。</span><span class="sxs-lookup"><span data-stu-id="81780-113">The bookmark of the first row.</span></span>|
|<span data-ttu-id="81780-114">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="81780-114">*Bookmark2*</span></span> |<span data-ttu-id="81780-115">2 番目の行のブックマークです。</span><span class="sxs-lookup"><span data-stu-id="81780-115">The bookmark of the second row.</span></span>|

## <a name="remarks"></a><span data-ttu-id="81780-116">解説</span><span class="sxs-lookup"><span data-stu-id="81780-116">Remarks</span></span>

<span data-ttu-id="81780-p101">ブックマークは、同じ [Recordset](recordset-object-ado.md) オブジェクト、または **Recordset** オブジェクトとその [複製](clone-method-ado.md)に適用する必要があります。異なる **Recordset** オブジェクトのブックマークを比較した場合、同じソースまたはコマンドから作成されたブックマークであっても、信頼できる結果は得られません。また、基になるプロバイダーがブックマークの比較をサポートしていない **Recordset** オブジェクトの場合も、ブックマークを比較できません。</span><span class="sxs-lookup"><span data-stu-id="81780-p101">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md). You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command. Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="81780-p102">ブックマークは、 **Recordset** オブジェクトの行を一意に識別します。カレント行のブックマークを取得するには、カレント行の [Bookmark](bookmark-property-ado.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="81780-p102">A bookmark uniquely identifies a row in a **Recordset** object. Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="81780-122">ブックマークのデータ型はプロバイダー固有であり、ADO ではバリアント (Variant) 型として公開されます。</span><span class="sxs-lookup"><span data-stu-id="81780-122">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="81780-123">たとえば、SQL Server のブックマークは DBTYPE\_R8 (二重)。</span><span class="sxs-lookup"><span data-stu-id="81780-123">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="81780-124">ADO では、このデータ型は、サブタイプが倍精度浮動小数点型のバリアント型として表されます。</span><span class="sxs-lookup"><span data-stu-id="81780-124">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="81780-p104">ブックマークを比較するとき、ADO はどのような種類の強制も試みません。値は、比較が行われるプロバイダーにそのまま渡されます。 **CompareBookmarks** メソッドに渡されるブックマークが異なる型の変数に格納されている場合は、"引数が間違った型、許容範囲外、または競合しています。" という型不一致エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="81780-p104">When comparing bookmarks, ADO does not attempt any type of coercion. The values are simply passed to the provider where the compare occurs. If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="81780-128">無効なブックマークや、形式が正しくないブックマークは、エラーの原因になります。</span><span class="sxs-lookup"><span data-stu-id="81780-128">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>

