---
title: onError イベント (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712177"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="0b653-102">onError イベント (RDS)</span><span class="sxs-lookup"><span data-stu-id="0b653-102">onError event (RDS)</span></span>

<span data-ttu-id="0b653-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0b653-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0b653-104">**onError** イベントは、処理中にエラーが発生するたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0b653-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b653-105">構文</span><span class="sxs-lookup"><span data-stu-id="0b653-105">Syntax</span></span>

<span data-ttu-id="0b653-106">onError*SCode*、*説明*、*ソース*、 *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="0b653-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="0b653-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0b653-107">Parameters</span></span>

|<span data-ttu-id="0b653-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0b653-108">Parameter</span></span>|<span data-ttu-id="0b653-109">説明</span><span class="sxs-lookup"><span data-stu-id="0b653-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0b653-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="0b653-110">*SCode*</span></span> |<span data-ttu-id="0b653-111">エラーの状態コードを表す整数型の値です。</span><span class="sxs-lookup"><span data-stu-id="0b653-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="0b653-112">*Description*</span><span class="sxs-lookup"><span data-stu-id="0b653-112">*Description*</span></span> |<span data-ttu-id="0b653-113">エラーの説明を表す文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="0b653-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="0b653-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="0b653-114">*Source*</span></span> |<span data-ttu-id="0b653-115">エラーを発生させたクエリまたはコマンドを表す文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="0b653-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="0b653-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="0b653-116">*CancelDisplay*</span></span> |<span data-ttu-id="0b653-117">ブール型 ( **Boolean** ) の値であり、 **True** に設定するとダイアログ ボックスにエラーが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="0b653-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

