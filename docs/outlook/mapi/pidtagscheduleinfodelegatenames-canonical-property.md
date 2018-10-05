---
title: PidTagScheduleInfoDelegateNames 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a257934411bb11a30378ee46317d323156f53e31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387294"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a>PidTagScheduleInfoDelegateNames 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
代理人の名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SCHDINFO_DELEGATE_NAMES、PR_SCHDINFO_DELEGATE_NAMES_A、PR_SCHDINFO_DELEGATE_NAMES_W  <br/> |
|識別子:  <br/> |0x6844  <br/> |
|データの種類 :   <br/> |PT_MV_STRING8、PT_MV_UNICODE  <br/> |
|エリア:  <br/> |空き/予約済み  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティ内の各エントリには、各デリゲートのアドレス帳の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値を含める必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> 接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

