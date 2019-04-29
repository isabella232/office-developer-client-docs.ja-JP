---
title: プロファイルのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424729"
---
# <a name="copying-a-profile"></a>プロファイルのコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルを作成する方法の1つは、既存のプロファイルからコピーして、必要なメッセージサービスおよびサービスプロバイダーを変更することです。 プロファイルのコピーには、 [MAPIAdminProfiles](mapiadminprofiles.md)関数を使用して MAPI で提供されるプロファイル管理オブジェクトを使用します。 
  
 **プロファイルをコピーするには**
  
1. **MAPIAdminProfiles**を呼び出して、 **IProfAdmin**インターフェイスポインターを取得します。 
    
2. プロファイルテーブルにアクセスするには、 [IProfAdmin:: getprofiletable](iprofadmin-getprofiletable.md)を呼び出します。 
    
3. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) をコピーするプロファイルの名前と一致させるために、 [spropertyrestriction](spropertyrestriction.md)構造のプロパティ制限を構築します。 
    
4. [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出して、プロファイルテーブルで該当する行を見つけます。 
    
5. [IProfAdmin:: copyprofile](iprofadmin-copyprofile.md)を呼び出し、 **PR_DISPLAY_NAME**列の値を_lpszoldprofilename_パラメーターとして渡します。 
    

