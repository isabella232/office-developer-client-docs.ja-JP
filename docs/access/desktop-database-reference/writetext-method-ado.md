---
title: WriteText メソッド (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6aecdbee544d3b30a6f6386c98d3083bb1167539
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949804"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="f22a9-102">WriteText メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="f22a9-102">WriteText method (ADO)</span></span>

<span data-ttu-id="f22a9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f22a9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f22a9-104">指定されたテキスト文字列を [Stream](stream-object-ado.md) オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="f22a9-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f22a9-105">構文</span><span class="sxs-lookup"><span data-stu-id="f22a9-105">Syntax</span></span>

<span data-ttu-id="f22a9-106">*ストリーム*。WriteText*データ*、*オプション*</span><span class="sxs-lookup"><span data-stu-id="f22a9-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="f22a9-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f22a9-107">Parameters</span></span>

|<span data-ttu-id="f22a9-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f22a9-108">Parameter</span></span>|<span data-ttu-id="f22a9-109">説明</span><span class="sxs-lookup"><span data-stu-id="f22a9-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f22a9-110">*Data*</span><span class="sxs-lookup"><span data-stu-id="f22a9-110">*Data*</span></span> |<span data-ttu-id="f22a9-111">書き込むテキストが格納された文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f22a9-111">A **String** value that contains the text in characters to be written.</span></span>|
|<span data-ttu-id="f22a9-112">*Options*</span><span class="sxs-lookup"><span data-stu-id="f22a9-112">*Options*</span></span> |<span data-ttu-id="f22a9-p101">省略可能です。指定された文字列の末尾に行区切り文字を書き込むかどうかを指定する [StreamWriteEnum](streamwriteenum.md) 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f22a9-p101">Optional. A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f22a9-115">解説</span><span class="sxs-lookup"><span data-stu-id="f22a9-115">Remarks</span></span>

<span data-ttu-id="f22a9-116">指定した文字列が、各文字列間にスペースや文字を挿入することなく **Stream** オブジェクトに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="f22a9-116">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="f22a9-p102">カレント [Position](position-property-ado.md) は、書き込まれたデータの次の文字に設定されます。 **WriteText** メソッドがストリーム内の残りのデータを切り捨てることはありません。後ろの文字を切り捨てるには、 [SetEOS](seteos-method-ado.md) を呼び出してください。</span><span class="sxs-lookup"><span data-stu-id="f22a9-p102">The current [Position](position-property-ado.md) is set to the character following the written data. The **WriteText** method does not truncate the rest of the data in a stream. If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="f22a9-120">現在の [EOS](eos-property-ado.md) 位置を越えて書き込みを行うと、新しい文字がすべて格納できるように [Stream](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) の **Size** が大きくなり、 **EOS** が **Stream** 内の新しい末尾バイトへと移動します。</span><span class="sxs-lookup"><span data-stu-id="f22a9-120">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="f22a9-p103">**WriteText** メソッドは、テキスト ストリーム ([Type](type-property-ado-stream.md) が **adTypeText**) で使用します。バイナリ ストリーム (**Type** が **adTypeBinary**) の場合は、[Write](write-method-ado.md) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f22a9-p103">The **WriteText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**). For binary streams (**Type** is **adTypeBinary**), use [Write](write-method-ado.md).</span></span>


