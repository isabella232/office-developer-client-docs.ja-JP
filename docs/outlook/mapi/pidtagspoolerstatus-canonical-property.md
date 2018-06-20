---
title: PidTagSpoolerStatus の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: df52f668e91b707c0436b394186b27fdbb3a5dbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803574"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>PidTagSpoolerStatus の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
MAPI スプーラーを無効に提供される情報に基づいて、メッセージのステータスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SPOOLER_STATUS  <br/> |
|識別子:  <br/> |0x0E10  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージ オブジェクトを MAPI によって計算されます。
  
このプロパティは、受信したメッセージのみが表示され、他のすべてのケースで予約されています。 最終的な場所に、メッセージが配信されたかどうか、またはかどうかメッセージ フック プロバイダー可能性があるメッセージを削除して再ルーティング中にそのことを示します。
  
クライアント アプリケーションでは、このプロパティを設定する必要があることはありません。 受信メッセージでは、クライアントまたはサービス プロバイダーは、メッセージの状態を確認するには、このプロパティに[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すことができます。 値 S_OK は、メッセージがメッセージ ・ ストアに正常に配信されたことを示します。 MAPI_E_OBJECT_DELETED の値は、メッセージは削除され、ストアにコミットされていないことを示します。 
  
メッセージ ストア プロバイダーは、メッセージ、受信者テーブル、および発信キューのテーブルでこのプロパティをサポートする必要があります。 クライアントとプロバイダーが発信キュー テーブルに列を設定し、制限する必要がありますこのプロパティに基づいています。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

