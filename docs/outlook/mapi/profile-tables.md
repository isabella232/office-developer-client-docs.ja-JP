---
title: プロファイルテーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328561"
---
# <a name="profile-tables"></a>プロファイルテーブル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルテーブルには、特定のクライアントアプリケーションに関連付けられているすべてのプロファイルに関する情報が表示されます。 クライアントが使用するために MAPI によって実装された、すべてのセッションに対して1つのプロファイルテーブルがあります。 
  
クライアントは、 [IProfAdmin:: getprofiletable](iprofadmin-getprofiletable.md)メソッドを呼び出して、プロファイルテーブルにアクセスします。 
  
プロファイルテーブルは、静的なテーブルです。 削除対象としてマークされているプロファイルは、プロファイルテーブルに含まれていません。
  
ほとんどのテーブル実装と同様に、 **getprofiletable**が呼び出され、クライアントが使用できるプロファイルがない場合、テーブルは0行で作成されます。 
  
次のプロパティを使用して、プロファイルテーブルで必要な列セットを作成します。
  
 **PR_DEFAULT_PROFILE**([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

