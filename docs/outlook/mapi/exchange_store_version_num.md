---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 00d92f8e2ec3af766d5b241d1a911be304b346d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800017"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="a8ea4-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="a8ea4-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="a8ea4-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8ea4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8ea4-105">Microsoft Office Outlook プロファイル内のアカウントが接続されている Microsoft Exchange Server のバージョン情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="a8ea4-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8ea4-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="a8ea4-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="a8ea4-107">Members</span><span class="sxs-lookup"><span data-stu-id="a8ea4-107">Members</span></span>

 <span data-ttu-id="a8ea4-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="a8ea4-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="a8ea4-109">リリースの機能に重要な新機能と変更が含まれる場合、一般に増加するメジャー バージョン番号です。</span><span class="sxs-lookup"><span data-stu-id="a8ea4-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="a8ea4-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="a8ea4-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="a8ea4-111">マイナー バージョン番号が特定のメジャー バージョン番号に対応して、リリースには、マイナーの新機能や重要な修正が含まれている場合が一般的に増加します。</span><span class="sxs-lookup"><span data-stu-id="a8ea4-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="a8ea4-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="a8ea4-112">_wBuild_</span></span>
  
- <span data-ttu-id="a8ea4-113">メジャー ビルド番号が特定のメジャーおよびマイナー バージョン番号に対応して、新機能や修正プログラムを含む内部のリリースでは一般にインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="a8ea4-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="a8ea4-114">リリースの主要な内部コードの分岐、またはマイルス トーンのリリース候補などときにも、この値がインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="a8ea4-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="a8ea4-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="a8ea4-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="a8ea4-116">内部リリースの新機能が含まれていますまたは主要なコードの分岐、またはマイルス トーンを示す特定の主要なビルドに対応する修正プログラムで一般に増加するマイナー ビルド番号です。</span><span class="sxs-lookup"><span data-stu-id="a8ea4-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8ea4-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8ea4-117">See also</span></span>



[<span data-ttu-id="a8ea4-118">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="a8ea4-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="a8ea4-119">PidTagProfileServerFullVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a8ea4-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

