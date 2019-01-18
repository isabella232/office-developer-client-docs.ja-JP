---
title: メソッドを ActiveX データ オブジェクト (ADO) を読む
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710889"
---
# <a name="read-method-ado"></a><span data-ttu-id="f65b3-102">Read メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="f65b3-102">Read method (ADO)</span></span>

<span data-ttu-id="f65b3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f65b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f65b3-104">バイナリ型の [Stream](stream-object-ado.md) オブジェクトから、指定されたバイト数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="f65b3-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f65b3-105">構文</span><span class="sxs-lookup"><span data-stu-id="f65b3-105">Syntax</span></span>

<span data-ttu-id="f65b3-106">*バリアント* = *ストリーム*。読み取り (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="f65b3-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="f65b3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f65b3-107">Parameters</span></span>

|<span data-ttu-id="f65b3-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f65b3-108">Parameter</span></span>|<span data-ttu-id="f65b3-109">説明</span><span class="sxs-lookup"><span data-stu-id="f65b3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f65b3-110">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="f65b3-110">*NumBytes*</span></span> |<span data-ttu-id="f65b3-p101">省略可能です。ファイルから読み取るバイト数を指定する長整数型 ( **Long** ) の値、または [StreamReadEnum](streamreadenum.md) 値の **adReadAll** (既定値) を指定します。</span><span class="sxs-lookup"><span data-stu-id="f65b3-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>|

## <a name="return-value"></a><span data-ttu-id="f65b3-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="f65b3-113">Return value</span></span>

<span data-ttu-id="f65b3-114">**Read** メソッドは、指定したバイト数またはストリーム全体を **Stream** オブジェクトから読み取り、結果のデータをバリアント型 ( **Variant** ) として返します。</span><span class="sxs-lookup"><span data-stu-id="f65b3-114">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f65b3-115">解説</span><span class="sxs-lookup"><span data-stu-id="f65b3-115">Remarks</span></span>

<span data-ttu-id="f65b3-p102">*NumBytes* が **Stream** に残っているバイト数よりも大きい場合、残っているバイトのみが返されます。読み取ったデータに、*NumBytes* で指定した長さに合うようにスペースが補充されることはありません。読み取るデータが残っていない場合は、Null 値のバリアント型が返されます。**Read** を使用して逆方向の読み取りを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="f65b3-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="f65b3-p103">*NumBytes* は常にバイトを表します。テキストの **Stream** オブジェクト ([Type](type-property-ado-stream.md) が **adTypeText**) の場合は、[ReadText](readtext-method-ado.md) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f65b3-p103">*NumBytes* always measures bytes. For text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**), use [ReadText](readtext-method-ado.md).</span></span>


