---
title: PidTagStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 68ab44134fd26f4a29b3048126bae73bf4dd0c82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599411"
---
# <a name="pidtagstatus-canonical-property"></a>PidTagStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの状態を定義するフラグの 32 ビット ビットマスクが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATUS  <br/> |
|識別子:  <br/> |0x360B  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI コンテナー  <br/> |
   
## <a name="remarks"></a>注釈

フォルダーのこのプロパティは、メッセージの PR_MSG_STATUS **(** [PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティに類似しています。 そのフラグはクライアント アプリケーションにのみ提供され、メッセージ ストアには影響を与えかねない。 クライアントは、これらの設定を使用または無視できます。 クライアントは、このプロパティのクライアント定義可能なビットに対して独自の値を定義することもできます。
  
ビットマスクには、次のフラグを 1 つ以上設定できます。
  
FLDSTATUS_DELMARKED 
  
> フォルダーは削除のマークが付きます。 クライアント アプリケーションは、このフラグを設定します。
    
FLDSTATUS_HIDDEN 
  
> フォルダーは非表示です。
    
FLDSTATUS_HIGHLIGHTED 
  
> フォルダーが強調表示されます 。たとえば、逆ビデオで表示されます。
    
FLDSTATUS_TAGGED 
  
> フォルダーにタグが付きます。
    
メッセージ ストア プロバイダーは、フォルダー上のこのプロパティを 1 つ以上のこれらの値に設定し、クライアントはアプリケーションに合った状態を解釈します。 たとえば、クライアントはフォルダーの状態を使用して階層テーブル内のフォルダーを視覚的に区別し、同じ状態のフォルダーを同じ方法で表示できます。 強調表示されたフォルダーは、リバース ビデオで表示できます。タグ付けされたフォルダーと削除マークが付いたフォルダーは、意味のあるアイコンで表示し、非表示のフォルダーを非表示にできます。
  
このプロパティのビット 16 ~ 31 ("0x10000" ~ "0x80000000") は、IPM クライアント アプリケーションで使用できます。 その他のすべてのビットは、MAPI で使用するために予約されています。前のリストで定義されていない値は、最初は 0 に設定し、変更する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
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

