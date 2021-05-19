---
title: プロファイル テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424351"
---
# <a name="profile-tables"></a>プロファイル テーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル テーブルには、特定のクライアント アプリケーションに関連付けられているすべてのプロファイルに関する情報が一覧表示されます。 クライアントで使用するために MAPI によって実装される、すべてのセッションに 1 つのプロファイル テーブルがあります。 
  
クライアントは [、IProfAdmin::GetProfileTable メソッド](iprofadmin-getprofiletable.md) を呼び出してプロファイル テーブルにアクセスします。 
  
プロファイル テーブルは静的テーブルです。 削除のマークが付いているプロファイルは、プロファイル テーブルには含まれません。
  
ほとんどのテーブル実装と同様に **、GetProfileTable** が呼び出され、クライアントで使用できるプロファイルがない場合、テーブルはゼロ行で作成されます。 
  
次のプロパティは、プロファイル テーブルで必要な列セットを構成します。
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

