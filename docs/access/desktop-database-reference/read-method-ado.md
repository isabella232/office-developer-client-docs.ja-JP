---
title: Read メソッド-ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307673"
---
# <a name="read-method-ado"></a><span data-ttu-id="8ba07-102">Read メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ba07-102">Read method (ADO)</span></span>

<span data-ttu-id="8ba07-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ba07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ba07-104">バイナリ型の [Stream](stream-object-ado.md) オブジェクトから、指定されたバイト数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="8ba07-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba07-105">構文</span><span class="sxs-lookup"><span data-stu-id="8ba07-105">Syntax</span></span>

<span data-ttu-id="8ba07-106">*バリアント型* = の*ストリーム*。読み取り (*numbytes* )</span><span class="sxs-lookup"><span data-stu-id="8ba07-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="8ba07-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8ba07-107">Parameters</span></span>

|<span data-ttu-id="8ba07-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8ba07-108">Parameter</span></span>|<span data-ttu-id="8ba07-109">説明</span><span class="sxs-lookup"><span data-stu-id="8ba07-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8ba07-110">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="8ba07-110">*NumBytes*</span></span> |<span data-ttu-id="8ba07-p101">省略可能です。ファイルから読み取るバイト数を指定する長整数型 ( **Long** ) の値、または [StreamReadEnum](streamreadenum.md) 値の **adReadAll** (既定値) を指定します。</span><span class="sxs-lookup"><span data-stu-id="8ba07-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>|

## <a name="return-value"></a><span data-ttu-id="8ba07-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="8ba07-113">Return value</span></span>

<span data-ttu-id="8ba07-114">**Read** メソッドは、指定したバイト数またはストリーム全体を **Stream** オブジェクトから読み取り、結果のデータをバリアント型 (**Variant**) として返します。</span><span class="sxs-lookup"><span data-stu-id="8ba07-114">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba07-115">注釈</span><span class="sxs-lookup"><span data-stu-id="8ba07-115">Remarks</span></span>

<span data-ttu-id="8ba07-p102">*NumBytes* が **Stream** に残っているバイト数よりも大きい場合、残っているバイトのみが返されます。読み取ったデータに、*NumBytes* で指定した長さに合うようにスペースが補充されることはありません。読み取るデータが残っていない場合は、Null 値のバリアント型が返されます。**Read** を使用して逆方向の読み取りを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="8ba07-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="8ba07-120">*NumBytes* は常にバイトを表します。</span><span class="sxs-lookup"><span data-stu-id="8ba07-120">*NumBytes* always measures bytes.</span></span> <span data-ttu-id="8ba07-121">テキストの **Stream** オブジェクト ([Type](type-property-ado-stream.md) が **adTypeText**) の場合は、[ReadText](readtext-method-ado.md) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="8ba07-121">For text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**), use [ReadText](readtext-method-ado.md).</span></span>


