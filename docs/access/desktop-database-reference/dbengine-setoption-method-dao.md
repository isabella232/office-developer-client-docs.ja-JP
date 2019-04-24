---
title: DBEngine メソッド (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5875a8935b1b44c3c36b29344af32df552f6e01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294198"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="88e64-102">DBEngine メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="88e64-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="88e64-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="88e64-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88e64-104">Windows レジストリに登録されている Microsoft Access データベース エンジンのキーの値を一時的に上書きします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="88e64-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="88e64-105">構文</span><span class="sxs-lookup"><span data-stu-id="88e64-105">Syntax</span></span>

<span data-ttu-id="88e64-106">*式*。SetOption (***オプション***、***値***)</span><span class="sxs-lookup"><span data-stu-id="88e64-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="88e64-107">\*式\***DBEngine**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="88e64-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="88e64-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="88e64-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88e64-109">名前</span><span class="sxs-lookup"><span data-stu-id="88e64-109">Name</span></span></p></th>
<th><p><span data-ttu-id="88e64-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="88e64-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="88e64-111">データ型</span><span class="sxs-lookup"><span data-stu-id="88e64-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="88e64-112">説明</span><span class="sxs-lookup"><span data-stu-id="88e64-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88e64-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="88e64-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="88e64-114">必須</span><span class="sxs-lookup"><span data-stu-id="88e64-114">Required</span></span></p></td>
<td><p><span data-ttu-id="88e64-115"><strong>Long 型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-116">「解説」で説明している定数です。</span><span class="sxs-lookup"><span data-stu-id="88e64-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e64-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="88e64-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="88e64-118">必須</span><span class="sxs-lookup"><span data-stu-id="88e64-118">Required</span></span></p></td>
<td><p><span data-ttu-id="88e64-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-120">オプションに設定する値を指定します。</span><span class="sxs-lookup"><span data-stu-id="88e64-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="88e64-121">注釈</span><span class="sxs-lookup"><span data-stu-id="88e64-121">Remarks</span></span>

<span data-ttu-id="88e64-122">各\_定数は、パス HKEY ローカル\_コンピューター\\ソフトウェア\\の Microsoft\\Office\\12.0\\access Connectivity Engine Engine\\\\ACE (つまりは、**dbsharedasyncdelay**は\_キーの HKEY ローカル\_コンピューター\\ソフトウェア\\Microsoft\\Office\\12.0\\access Connectivity Engine\\エンジン\\ACE に対応します。\\sharedasyncdelay など)。</span><span class="sxs-lookup"><span data-stu-id="88e64-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88e64-123">定数</span><span class="sxs-lookup"><span data-stu-id="88e64-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="88e64-124">説明</span><span class="sxs-lookup"><span data-stu-id="88e64-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88e64-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-126">PageTimeout キー</span><span class="sxs-lookup"><span data-stu-id="88e64-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e64-127"><strong>dbsharedasyncdelay</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-128">SharedAsyncDelay キー</span><span class="sxs-lookup"><span data-stu-id="88e64-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88e64-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-130">ExclusiveAsyncDelay キー</span><span class="sxs-lookup"><span data-stu-id="88e64-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e64-131"><strong>dblockretry</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-132">LockRetry キー</span><span class="sxs-lookup"><span data-stu-id="88e64-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88e64-133"><strong>dbusercommitsync</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-134">UserCommitSync キー</span><span class="sxs-lookup"><span data-stu-id="88e64-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e64-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-136">ImplicitCommitSync キー</span><span class="sxs-lookup"><span data-stu-id="88e64-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88e64-137"><strong>dbmaxbuffersize</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-138">MaxBufferSize キー</span><span class="sxs-lookup"><span data-stu-id="88e64-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e64-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-140">MaxLocksPerFile キー</span><span class="sxs-lookup"><span data-stu-id="88e64-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88e64-141"><strong>dblockdelay</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-142">LockDelay キー</span><span class="sxs-lookup"><span data-stu-id="88e64-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88e64-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-144">RecycleLVs キー</span><span class="sxs-lookup"><span data-stu-id="88e64-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88e64-145"><strong>dbflushtransactiontimeout</strong></span><span class="sxs-lookup"><span data-stu-id="88e64-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="88e64-146">FlushTransactionTimeout キー</span><span class="sxs-lookup"><span data-stu-id="88e64-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="88e64-p101">**SetOption** メソッドを使用して、実行時にレジストリ値を上書きします。 **SetOption** メソッドで設定された新しい値は、 **SetOption** に対する別の呼び出しによって値が再度変更されるか、 **DBEngine** オブジェクトが閉じられるまで有効です。</span><span class="sxs-lookup"><span data-stu-id="88e64-p101">Use the **SetOption** method to override registry values at run-time. New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

