---
title: PidLidDistributionListMembers 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335071"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>PidLidDistributionListMembers 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用配布リストのメンバーに対応するオブジェクトの entryids のリストを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispiddlmembers  <br/> |
|プロパティセット:  <br/> |PSETID_Address  <br/> |
|ロング ID (LID):  <br/> |0x00008055  <br/> |
|データの種類 :   <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

個人用配布リストのメンバーは、他の個人用配布リスト、連絡先に含まれている電子アドレス、グローバルアドレス一覧のユーザーまたは配布リスト、または1回限りの電子メールアドレスにすることができます。 各 entryid の形式は、 [[OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)で指定された1回限りの entryid であるか、またはラップされた entryid である必要があります。 
  
このプロパティを設定する場合、クライアントまたはサーバーの合計サイズが15000バイト未満であることを確認する必要があります。
  
このプロパティは、個人用配布リストのメンバーに対応する1回限りの entryids のリストを指定します。 これらの1回限りの entryids は、個人用配布リストのメンバーの表示名と電子メールアドレスをカプセル化します。
  
クライアントまたはサーバーでこのプロパティが設定されている場合は、 **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) プロパティのエントリごとに、このプロパティ**dispiddlmembers**と同期する必要があります。**dispidDLOneOffMembers**内での同じ位置。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

