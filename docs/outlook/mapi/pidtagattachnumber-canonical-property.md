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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327252"
---
# <a name="pidtagattachnumber-canonical-property"></a>PidTagAttachNumber 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
親メッセージ内の添付ファイルを一意に識別する番号を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_NUM  <br/> |
|識別子:  <br/> |0x0e21  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

メッセージストアは、このプロパティを生成して管理します。 添付ファイルの番号は、描画位置の後の2番目の並べ替えキーです (添付ファイルテーブル内)。 
  
 **PR_ATTACH_NUM**は、 [IMessage:: openattach](imessage-openattach.md)メソッドを使用して添付ファイルを開くために使用されます。 クライアントアプリケーションのセッションでは、添付ファイルテーブルが開いている間は、メッセージの添付ファイルの**PR_ATTACH_NUM**プロパティは一定のままです。 
  
メッセージストアは、 **IMessage:: createattach**および**IMessage::D eleteattach**メソッドを使用して、変更内容をテーブルに反映します。 このオプションでは、メッセージストアは、クライアントがそれらの変更に再同期できるように、開いている添付ファイルテーブルでテーブル通知を生成できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

