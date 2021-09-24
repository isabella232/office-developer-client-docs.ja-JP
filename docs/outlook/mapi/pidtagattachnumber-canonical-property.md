---
title: PidTagAttachNumber 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b594a7cd69b6c75b064e30868f3cce0070519246
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550835"
---
# <a name="pidtagattachnumber-canonical-property"></a>PidTagAttachNumber 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
親メッセージ内の添付ファイルを一意に識別する番号を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_NUM  <br/> |
|識別子:  <br/> |0x0E21  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

メッセージ ストアは、このプロパティを生成および管理します。 添付ファイル番号は、添付ファイル テーブルのレンダリング位置の後のセカンダリ 並べ替えキーです。 
  
 **PR_ATTACH_NUM** は [、IMessage::OpenAttach](imessage-openattach.md) メソッドを使用して添付ファイルを開くのに使用されます。 クライアント アプリケーションのセッション内では、PR_ATTACH_NUM **テーブルが** 開いている限り、メッセージ添付ファイルのプロパティは一定のままです。 
  
メッセージ ストアは **、IMessage::CreateAttach** メソッドと **IMessage::D eleteAttach** メソッドを使用してテーブルに変更を伝達します。 そのオプションで、メッセージ ストアは開いている添付ファイル テーブルにテーブル通知を生成して、クライアントがそれらの変更に再同期できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

