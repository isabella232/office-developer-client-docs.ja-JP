---
title: PidTagAttachNumber の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c4a46710311f2c4d26ec3d667c7bf535df69f595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802488"
---
# <a name="pidtagattachnumber-canonical-property"></a>PidTagAttachNumber の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
その親メッセージ内の添付ファイルを一意に識別する番号が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ATTACH_NUM  <br/> |
|識別子:  <br/> |0x0E21  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>備考

メッセージ ・ ストアを生成し、このプロパティを管理します。 添付ファイル数が、添付ファイル テーブル内のレンダリング位置、2 番目の並べ替えキー。 
  
 [IMessage::OpenAttach](imessage-openattach.md)メソッドを使用して添付ファイルを開くには、 **PR_ATTACH_NUM**が使用されます。 添付ファイル テーブルが開いている限り、クライアント アプリケーションのセッション内で一定のまま、メッセージの添付ファイルの**PR_ATTACH_NUM**プロパティ。 
  
メッセージ ・ ストアでは、 **IMessage::CreateAttach**メソッドと**IMessage::DeleteAttach**メソッドを使用して、テーブルへの変更が反映されます。 オプションで、メッセージ ・ ストアはクライアントがそれらの変更を再同期化できるように、添付ファイルを開くテーブル上のテーブルの通知を生成できます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

