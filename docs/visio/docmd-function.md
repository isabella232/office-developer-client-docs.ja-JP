---
title: DOCMD 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: 識別されたコマンドを実行します。
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315233"
---
# <a name="docmd-function"></a><span data-ttu-id="17137-103">DOCMD 関数</span><span class="sxs-lookup"><span data-stu-id="17137-103">DOCMD Function</span></span>

<span data-ttu-id="17137-104">識別されたコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="17137-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="17137-105">構文</span><span class="sxs-lookup"><span data-stu-id="17137-105">Syntax</span></span>

 <span data-ttu-id="17137-106">**DOCMD**( _commandID_)</span><span class="sxs-lookup"><span data-stu-id="17137-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="17137-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="17137-107">Parameters</span></span>

|<span data-ttu-id="17137-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="17137-108">**Name**</span></span>|<span data-ttu-id="17137-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="17137-109">**Required/Optional**</span></span>|<span data-ttu-id="17137-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="17137-110">**Data Type**</span></span>|<span data-ttu-id="17137-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="17137-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="17137-112">_commandID_</span><span class="sxs-lookup"><span data-stu-id="17137-112">_commandID_</span></span> <br/> |<span data-ttu-id="17137-113">必須</span><span class="sxs-lookup"><span data-stu-id="17137-113">Required</span></span>  <br/> |<span data-ttu-id="17137-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="17137-114">**Number**</span></span> <br/> | <span data-ttu-id="17137-115">実行するコマンドを指定します。</span><span class="sxs-lookup"><span data-stu-id="17137-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17137-116">解説</span><span class="sxs-lookup"><span data-stu-id="17137-116">Remarks</span></span>

<span data-ttu-id="17137-117">docmd 関数でサポートされているコマンドの一覧については、Microsoft Visio 2013 Automation リファレンスのトピック「docmd/docmd コマンド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17137-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="17137-118">例</span><span class="sxs-lookup"><span data-stu-id="17137-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="17137-119">[**図形データ**] ダイアログ ボックスをユーザー インターフェイスに表示します。</span><span class="sxs-lookup"><span data-stu-id="17137-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

