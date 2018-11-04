---
title: onError イベント (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a61ec584f5baddcfdb8ce1f6dda1bf990546c053
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949356"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="84f41-102">onError イベント (RDS)</span><span class="sxs-lookup"><span data-stu-id="84f41-102">onError event (RDS)</span></span>

<span data-ttu-id="84f41-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="84f41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84f41-104">**onError** イベントは、処理中にエラーが発生するたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84f41-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f41-105">構文</span><span class="sxs-lookup"><span data-stu-id="84f41-105">Syntax</span></span>

<span data-ttu-id="84f41-106">onError*SCode*、*説明*、*ソース*、 *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="84f41-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="84f41-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84f41-107">Parameters</span></span>

|<span data-ttu-id="84f41-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84f41-108">Parameter</span></span>|<span data-ttu-id="84f41-109">説明</span><span class="sxs-lookup"><span data-stu-id="84f41-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="84f41-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="84f41-110">*SCode*</span></span> |<span data-ttu-id="84f41-111">エラーの状態コードを表す整数型の値です。</span><span class="sxs-lookup"><span data-stu-id="84f41-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="84f41-112">*Description*</span><span class="sxs-lookup"><span data-stu-id="84f41-112">*Description*</span></span> |<span data-ttu-id="84f41-113">エラーの説明を表す文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="84f41-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="84f41-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="84f41-114">*Source*</span></span> |<span data-ttu-id="84f41-115">エラーを発生させたクエリまたはコマンドを表す文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="84f41-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="84f41-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="84f41-116">*CancelDisplay*</span></span> |<span data-ttu-id="84f41-117">ブール型 ( **Boolean** ) の値であり、 **True** に設定するとダイアログ ボックスにエラーが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="84f41-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

