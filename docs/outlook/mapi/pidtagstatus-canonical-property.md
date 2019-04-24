---
title: PidTagStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278793"
---
# <a name="pidtagstatus-canonical-property"></a>PidTagStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの状態を定義するフラグの32ビットビットマスクを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATUS  <br/> |
|識別子:  <br/> |0x360b  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI コンテナー  <br/> |
   
## <a name="remarks"></a>解説

フォルダーのこのプロパティは、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティに似ています。 このフラグは、クライアントアプリケーションに対してのみ提供され、メッセージストアには影響しません。 クライアントは、これらの設定を使用または無視できます。 クライアントは、このプロパティのクライアントで定義可能なビットに対して独自の値を定義することもできます。
  
ビットマスクには、次の1つ以上のフラグを設定できます。
  
FLDSTATUS_DELMARKED 
  
> フォルダーは削除するように設定されています。 クライアントアプリケーションがこのフラグを設定します。
    
FLDSTATUS_HIDDEN 
  
> フォルダーは表示されません。
    
FLDSTATUS_HIGHLIGHTED 
  
> フォルダーが強調表示されます。たとえば、[リバースビデオ] に示されています。
    
FLDSTATUS_TAGGED 
  
> フォルダーにタグが付けられます。
    
メッセージストアプロバイダーは、フォルダーのこのプロパティをこれらの値の1つ以上に設定し、クライアントはアプリケーションに応じて状態を解釈します。 たとえば、クライアントはフォルダーの状態を使用して、階層テーブル内のフォルダーを視覚的に区別し、同じ状態のフォルダーを同じ方法で表示することができます。 強調表示されたフォルダーを反転表示することができます。タグ付きフォルダーや削除用のマークが付いたフォルダーは、わかりやすいアイコンで表示できます。隠しフォルダーは非表示にすることができます。
  
このプロパティのビット16から 31 (";" ~ "0x80000000") は、IPM クライアントアプリケーションで使用できます。 他のすべてのビットは MAPI での使用のために予約されています。前述のリストで定義されていないものは、最初は0に設定され、変更されません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
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

