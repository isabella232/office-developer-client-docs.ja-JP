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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389968"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>PidLidDistributionListMembers 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用配布リストのメンバーに対応するオブジェクトのエントリ Id の一覧を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidDLMembers  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008055  <br/> |
|データの種類 :   <br/> |PT_MV_BINARY  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>備考

個人用配布リストのメンバーには、他の個人用配布リスト、連絡先、グローバル アドレス一覧のユーザーまたは配布リスト、または 1 回限りの電子メール アドレスに含まれている電子メールのアドレスを指定できます。 各エントリ Id の形式は、 [MS-OXCDATA](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)で指定されている、1 回限りのエントリ Id またはラップのエントリ Id のいずれかにする必要があります。 
  
このプロパティを設定するとき、クライアントまたはサーバーを保証しなければならないの合計サイズ 15,000 バイト未満です。
  
このプロパティは、個人用配布リストのメンバーに対応する 1 回限りのエントリ Id の一覧を指定します。 これらの一時エントリ Id は、表示名と個人用配布リストのメンバーの電子メール アドレスをカプセル化します。
  
**DispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) のプロパティの各エントリに対してこのプロパティ**dispidDLMembers**同期する必要があるクライアントまたはサーバーは、このプロパティを設定する場合は、内のエントリが存在する必要があります、**dispidDLOneOffMembers**内の同じ位置です。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

