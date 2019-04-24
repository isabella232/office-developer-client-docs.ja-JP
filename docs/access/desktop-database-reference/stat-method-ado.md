---
title: Stat メソッド-ActiveX データオブジェクト (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308551"
---
# <a name="stat-method-ado"></a><span data-ttu-id="15c9c-102">Stat メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="15c9c-102">Stat method (ADO)</span></span>

<span data-ttu-id="15c9c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="15c9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="15c9c-104">**Stream** オブジェクトの情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="15c9c-104">Retrieves information about a **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c9c-105">構文</span><span class="sxs-lookup"><span data-stu-id="15c9c-105">Syntax</span></span>

<span data-ttu-id="15c9c-106">長い*ストリーム*。Stat (*StatStg*, *statflag*)</span><span class="sxs-lookup"><span data-stu-id="15c9c-106">Long *stream*.Stat(*StatStg*, *StatFlag*)</span></span>

## <a name="return-value"></a><span data-ttu-id="15c9c-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="15c9c-107">Return value</span></span>

<span data-ttu-id="15c9c-108">操作の状態を示す長整数型 (Long) の値。</span><span class="sxs-lookup"><span data-stu-id="15c9c-108">A long value indicating the status of the operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="15c9c-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="15c9c-109">Parameters</span></span>

|<span data-ttu-id="15c9c-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="15c9c-110">Parameter</span></span>|<span data-ttu-id="15c9c-111">説明</span><span class="sxs-lookup"><span data-stu-id="15c9c-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="15c9c-112">*StatStg*</span><span class="sxs-lookup"><span data-stu-id="15c9c-112">*StatStg*</span></span> |<span data-ttu-id="15c9c-p101">ストリームの情報が格納される STATSTG 構造体。ADO の Stream オブジェクトに使用される Stat メソッドの実装は、この構造体のすべてのフィールドに情報を格納するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="15c9c-p101">A STATSTG structure that will be filled in with information about the stream. The implementation of the Stat method used by the ADO Stream object does not fill in all of the fields of the structure.</span></span>|
|<span data-ttu-id="15c9c-115">*StatFlag*</span><span class="sxs-lookup"><span data-stu-id="15c9c-115">*StatFlag*</span></span> |<span data-ttu-id="15c9c-p102">STATSTG 構造体の一部のメンバーが返されないように指定して、メモリ割り当て操作を少なくします。このパラメーターには、STATFLAG 列挙の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="15c9c-p102">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation. Values are taken from the STATFLAG enumeration.</span></span><br/><br/><span data-ttu-id="15c9c-118">statflag 列挙体には、次の2つの値があります。</span><span class="sxs-lookup"><span data-stu-id="15c9c-118">The STATFLAG enumeration has two values:</span></span><br/><span data-ttu-id="15c9c-119">-STATFLAG_DEFAULT: 0</span><span class="sxs-lookup"><span data-stu-id="15c9c-119">- STATFLAG_DEFAULT: 0</span></span><br/><span data-ttu-id="15c9c-120">-STATFLAG_NONAME: 1</span><span class="sxs-lookup"><span data-stu-id="15c9c-120">- STATFLAG_NONAME: 1</span></span> |


## <a name="remarks"></a><span data-ttu-id="15c9c-121">注釈</span><span class="sxs-lookup"><span data-stu-id="15c9c-121">Remarks</span></span>

<span data-ttu-id="15c9c-122">ADO の Stream オブジェクト用に実装された Stat メソッドは、STATSTG 構造体の以下のフィールドに値を格納します。</span><span class="sxs-lookup"><span data-stu-id="15c9c-122">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:</span></span>

|<span data-ttu-id="15c9c-123">Field</span><span class="sxs-lookup"><span data-stu-id="15c9c-123">Field</span></span>|<span data-ttu-id="15c9c-124">説明</span><span class="sxs-lookup"><span data-stu-id="15c9c-124">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="15c9c-125">*pwcsName*</span><span class="sxs-lookup"><span data-stu-id="15c9c-125">*pwcsName*</span></span> |<span data-ttu-id="15c9c-126">ストリームの名前を含む文字列。使用可能な場合、statflag の値 statflag フラグ\_が指定されていない場合。</span><span class="sxs-lookup"><span data-stu-id="15c9c-126">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG\_NONAME was not specified.</span></span>|
|<span data-ttu-id="15c9c-127">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="15c9c-127">*cbSize*</span></span> |<span data-ttu-id="15c9c-128">ストリームまたはバイト配列のバイト単位でのサイズを示します。</span><span class="sxs-lookup"><span data-stu-id="15c9c-128">Specifies the size in bytes of the stream or byte array.</span></span>|
|<span data-ttu-id="15c9c-129">*mtime*</span><span class="sxs-lookup"><span data-stu-id="15c9c-129">*mtime*</span></span> |<span data-ttu-id="15c9c-130">この記憶域、ストリーム、またはバイト配列の最終変更時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="15c9c-130">Indicates the last modification time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="15c9c-131">*ctime*</span><span class="sxs-lookup"><span data-stu-id="15c9c-131">*ctime*</span></span> |<span data-ttu-id="15c9c-132">この記憶域、ストリーム、またはバイト配列の作成時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="15c9c-132">Indicates the creation time for this storage, stream, or byte array.</span></span>|
|<span data-ttu-id="15c9c-133">*atime*</span><span class="sxs-lookup"><span data-stu-id="15c9c-133">*atime*</span></span> |<span data-ttu-id="15c9c-134">この記憶域、ストリーム、またはバイト配列の最終アクセス時刻を示します。</span><span class="sxs-lookup"><span data-stu-id="15c9c-134">Indicates the last access time for this storage, stream or byte array.</span></span>|

<span data-ttu-id="15c9c-135">\_statflag が statflag パラメーターで指定されている場合、ストリームの名前は返されません。</span><span class="sxs-lookup"><span data-stu-id="15c9c-135">If STATFLAG\_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</span></span>

<span data-ttu-id="15c9c-136">\_statflag が statflag パラメーターで指定されておらず、現在のストリームに使用できる名前がない場合、この値は E\_NOTIMPL になります。</span><span class="sxs-lookup"><span data-stu-id="15c9c-136">If STATFLAG\_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E\_NOTIMPL.</span></span>

