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
description: 指定されたコマンドを実行します。
ms.openlocfilehash: e425dd9605c18d4647787c5df7aeaa4fd5f9e4cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805245"
---
# <a name="docmd-function"></a><span data-ttu-id="28fb3-103">DOCMD 関数</span><span class="sxs-lookup"><span data-stu-id="28fb3-103">DOCMD Function</span></span>

<span data-ttu-id="28fb3-104">指定されたコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="28fb3-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="28fb3-105">構文</span><span class="sxs-lookup"><span data-stu-id="28fb3-105">Syntax</span></span>

 <span data-ttu-id="28fb3-106">**Docmd オブジェクト**( _commandid が_)</span><span class="sxs-lookup"><span data-stu-id="28fb3-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="28fb3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="28fb3-107">Parameters</span></span>

|<span data-ttu-id="28fb3-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="28fb3-108">**Name**</span></span>|<span data-ttu-id="28fb3-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="28fb3-109">**Required/Optional**</span></span>|<span data-ttu-id="28fb3-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="28fb3-110">**Data Type**</span></span>|<span data-ttu-id="28fb3-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="28fb3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28fb3-112">_commandid が_</span><span class="sxs-lookup"><span data-stu-id="28fb3-112">_commandID_</span></span> <br/> |<span data-ttu-id="28fb3-113">必須</span><span class="sxs-lookup"><span data-stu-id="28fb3-113">Required</span></span>  <br/> |<span data-ttu-id="28fb3-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="28fb3-114">**Number**</span></span> <br/> | <span data-ttu-id="28fb3-115">実行するコマンドを指定します。</span><span class="sxs-lookup"><span data-stu-id="28fb3-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28fb3-116">注釈</span><span class="sxs-lookup"><span data-stu-id="28fb3-116">Remarks</span></span>

<span data-ttu-id="28fb3-117">DOCMD 関数でサポートされているコマンドのリストは、Microsoft Visio 2013 『 オートメーション リファレンス 』 の「「DOCMD/DOCMD コマンド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="28fb3-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="28fb3-118">例</span><span class="sxs-lookup"><span data-stu-id="28fb3-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="28fb3-119">[**図形データ**] ダイアログ ボックスをユーザー インターフェイスに表示します。</span><span class="sxs-lookup"><span data-stu-id="28fb3-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

