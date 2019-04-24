---
title: ReadText メソッド (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 883f74c06da83a46f9ffd1c30861d796c04b5c74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300799"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="32247-102">ReadText メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="32247-102">ReadText method (ADO)</span></span>

<span data-ttu-id="32247-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="32247-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32247-104">文字列型の [Stream](stream-object-ado.md) オブジェクトから、指定された文字数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="32247-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="32247-105">構文</span><span class="sxs-lookup"><span data-stu-id="32247-105">Syntax</span></span>

<span data-ttu-id="32247-106">*文字列* = *ストリーム*。ReadText (*numchars*)</span><span class="sxs-lookup"><span data-stu-id="32247-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="32247-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="32247-107">Parameters</span></span>

|<span data-ttu-id="32247-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="32247-108">Parameter</span></span>|<span data-ttu-id="32247-109">説明</span><span class="sxs-lookup"><span data-stu-id="32247-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="32247-110">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="32247-110">*NumChars*</span></span> |<span data-ttu-id="32247-p101">省略可能です。ファイルから読み取る文字の数を指定する長整数型 ( **Long** ) の値、または [StreamReadEnum](streamreadenum.md) 値を指定します。既定値は **adReadAll** です。</span><span class="sxs-lookup"><span data-stu-id="32247-p101">Optional. A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value. The default value is **adReadAll**.</span></span>|

## <a name="return-value"></a><span data-ttu-id="32247-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="32247-114">Return value</span></span>

<span data-ttu-id="32247-115">**ReadText** メソッドは、指定した文字数、行全体、またはストリーム全体を **Stream** オブジェクトから読み取り、結果の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="32247-115">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="32247-116">注釈</span><span class="sxs-lookup"><span data-stu-id="32247-116">Remarks</span></span>

<span data-ttu-id="32247-p102">*NumChar* がストリームに残っている文字の数よりも大きい場合、残っている文字のみが返されます。読み取った文字列に、*NumChar* で指定した長さに合うようにスペースが補充されることはありません。読み取る文字が残っていない場合は、値が Null のバリアント型が返されます。**ReadText** は、逆方向の読み取りに使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="32247-p102">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned. The string read is not padded to match the length specified by *NumChar*. If there are no characters left to read, a variant whose value is null is returned. **ReadText** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="32247-121">**ReadText** メソッドは、文字列型ストリーム ([Type](type-property-ado-stream.md) が **adTypeText**) で使用します。</span><span class="sxs-lookup"><span data-stu-id="32247-121">The **ReadText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="32247-122">バイナリ型のストリーム (**Type** が **adTypeBinary**) の場合は、[Read](read-method-ado.md) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="32247-122">For binary streams (**Type** is **adTypeBinary**), use [Read](read-method-ado.md).</span></span>

