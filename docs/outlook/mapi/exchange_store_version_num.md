---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433725"
---
# <a name="exchange_store_version_num"></a><span data-ttu-id="8aa73-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="8aa73-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="8aa73-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8aa73-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8aa73-105">プロファイルが接続されているアカウントMicrosoft Exchange Serverのバージョン情報Microsoft Office Outlook格納します。</span><span class="sxs-lookup"><span data-stu-id="8aa73-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8aa73-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="8aa73-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="8aa73-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="8aa73-107">Members</span></span>

 <span data-ttu-id="8aa73-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="8aa73-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="8aa73-109">リリースに大幅な新機能と機能の変更が含まれている場合に一般的に増分されるメジャー バージョン番号。</span><span class="sxs-lookup"><span data-stu-id="8aa73-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="8aa73-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="8aa73-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="8aa73-111">特定のメジャー バージョン番号に対応するマイナー バージョン番号で、リリースにマイナーな新機能や大幅な修正が含まれている場合、通常は増分されます。</span><span class="sxs-lookup"><span data-stu-id="8aa73-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="8aa73-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="8aa73-112">_wBuild_</span></span>
  
- <span data-ttu-id="8aa73-113">特定のメジャー バージョン番号とマイナー バージョン番号に対応し、一般に、新機能または修正プログラムを含む内部リリースで増分されるメジャー ビルド番号。</span><span class="sxs-lookup"><span data-stu-id="8aa73-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="8aa73-114">この値は、リリースが主要な内部コードブランチまたはマイルストーン (リリース候補など) である場合にも増分されます。</span><span class="sxs-lookup"><span data-stu-id="8aa73-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="8aa73-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="8aa73-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="8aa73-116">メジャー コードブランチまたはマイルストーンを表す特定のメジャー ビルドに対応する新機能または修正プログラムを含む内部リリースで一般的に増分されるマイナービルド番号。</span><span class="sxs-lookup"><span data-stu-id="8aa73-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8aa73-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="8aa73-117">See also</span></span>



[<span data-ttu-id="8aa73-118">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="8aa73-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="8aa73-119">PidTagProfileServerFullVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8aa73-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

