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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287036"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="aaf1e-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="aaf1e-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="aaf1e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aaf1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aaf1e-105">microsoft Office Outlook プロファイルのアカウントが接続されている microsoft Exchange Server のバージョン情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="aaf1e-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aaf1e-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="aaf1e-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="aaf1e-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="aaf1e-107">Members</span></span>

 <span data-ttu-id="aaf1e-108">_wmajorversion_</span><span class="sxs-lookup"><span data-stu-id="aaf1e-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="aaf1e-109">リリースに重要な新機能と機能の変更が含まれている場合に、通常はメジャーバージョン番号がインクリメントされます。</span><span class="sxs-lookup"><span data-stu-id="aaf1e-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="aaf1e-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="aaf1e-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="aaf1e-111">特定のメジャーバージョン番号に対応するマイナーバージョン番号。リリースにマイナーな新機能や重要な修正が含まれている場合に、通常は増分されます。</span><span class="sxs-lookup"><span data-stu-id="aaf1e-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="aaf1e-112">_wbuild_</span><span class="sxs-lookup"><span data-stu-id="aaf1e-112">_wBuild_</span></span>
  
- <span data-ttu-id="aaf1e-113">特定のメジャーおよびマイナーバージョン番号に対応し、新しい機能またはフィックスを含む内部リリースで一般的にインクリメントされるメジャービルド番号。</span><span class="sxs-lookup"><span data-stu-id="aaf1e-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="aaf1e-114">この値は、リリース候補のように、リリースが主要な内部コード分岐またはマイルストーンの場合にも増加します。</span><span class="sxs-lookup"><span data-stu-id="aaf1e-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="aaf1e-115">_wminorbuild_</span><span class="sxs-lookup"><span data-stu-id="aaf1e-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="aaf1e-116">メジャーコード分岐またはマイルストーンを示す、特定の主要ビルドに対応する新機能またはフィックスを含む内部リリースで通常増分されるマイナービルド番号。</span><span class="sxs-lookup"><span data-stu-id="aaf1e-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aaf1e-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="aaf1e-117">See also</span></span>



[<span data-ttu-id="aaf1e-118">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="aaf1e-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="aaf1e-119">PidTagProfileServerFullVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="aaf1e-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

