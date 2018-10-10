---
title: onError イベント (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fe6f6b78297008e25e15dc17e243ae982a5ccf3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479329"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="b2c64-102">onError イベント (RDS)</span><span class="sxs-lookup"><span data-stu-id="b2c64-102">onError Event (RDS)</span></span>


<span data-ttu-id="b2c64-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2c64-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b2c64-104">**onError** イベントは、処理中にエラーが発生するたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b2c64-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c64-105">構文</span><span class="sxs-lookup"><span data-stu-id="b2c64-105">Syntax</span></span>

<span data-ttu-id="b2c64-106">onError*SCode*、*説明*、*ソース*、 *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="b2c64-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="b2c64-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2c64-107">Parameters</span></span>

  - <span data-ttu-id="b2c64-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="b2c64-108">*SCode*</span></span>

  - <span data-ttu-id="b2c64-109">エラーの状態コードを表す整数型の値です。</span><span class="sxs-lookup"><span data-stu-id="b2c64-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="b2c64-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="b2c64-110">*Description*</span></span>

  - <span data-ttu-id="b2c64-111">エラーの説明を表す文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="b2c64-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="b2c64-112">*Source*</span><span class="sxs-lookup"><span data-stu-id="b2c64-112">*Source*</span></span>

  - <span data-ttu-id="b2c64-113">エラーを発生させたクエリまたはコマンドを表す文字列型 ( **String** ) の値です。</span><span class="sxs-lookup"><span data-stu-id="b2c64-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="b2c64-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="b2c64-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="b2c64-115">ブール型 ( **Boolean** ) の値であり、 **True** に設定するとダイアログ ボックスにエラーが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b2c64-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

