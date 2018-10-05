---
title: PidTagAttachNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401504"
---
# <a name="pidtagattachnumber-canonical-property"></a>PidTagAttachNumber 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
その親メッセージ内の添付ファイルを一意に識別する番号が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_NUM  <br/> |
|識別子:  <br/> |0x0E21  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

メッセージ ・ ストアを生成し、このプロパティを管理します。 添付ファイル数が、添付ファイル テーブル内のレンダリング位置、2 番目の並べ替えキー。 
  
 [IMessage::OpenAttach](imessage-openattach.md)メソッドを使用して添付ファイルを開くには、 **PR_ATTACH_NUM**が使用されます。 添付ファイル テーブルが開いている限り、クライアント アプリケーションのセッション内で一定のまま、メッセージの添付ファイルの**PR_ATTACH_NUM**プロパティ。 
  
メッセージ ・ ストアでは、 **IMessage::CreateAttach**メソッドと**IMessage::DeleteAttach**メソッドを使用して、テーブルへの変更が反映されます。 オプションで、メッセージ ・ ストアはクライアントがそれらの変更を再同期化できるように、添付ファイルを開くテーブル上のテーブルの通知を生成できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

