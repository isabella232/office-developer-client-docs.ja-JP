---
title: プロファイル テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1046c8d92feec16428329636257ed9c1f0ec8719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571480"
---
# <a name="profile-tables"></a>プロファイル テーブル

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロファイルの一覧には、特定のクライアント アプリケーションに関連付けられているすべてのプロファイルに関する情報が表示されます。 1 つのプロファイル テーブルのすべてのセッションでは、クライアントが使用する MAPI によって実装されています。 
  
クライアントは、 [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)メソッドを呼び出して、プロファイル テーブルをアクセスします。 
  
プロファイル テーブルは、静的なテーブルです。 削除対象としてマークされているプロファイルは、プロファイル テーブルには含まれません。
  
としてテーブルのほとんどの実装で**GetProfileTable**が呼び出され、クライアントで利用できるプロファイルがない場合、テーブルが作成 0 個の行を持つ。 
  
次のプロパティは、プロファイル テーブルに設定する必要な列を構成します。
  
 **PR_DEFAULT_PROFILE**([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

