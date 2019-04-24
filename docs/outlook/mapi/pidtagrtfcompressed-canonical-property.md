---
title: PidTagRtfCompressed 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfCompressed
api_type:
- COM
ms.assetid: fd0ccb88-55ce-4d7c-9573-6e5d6239b6a8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357891"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>PidTagRtfCompressed 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常は圧縮形式のメッセージテキストのリッチテキスト形式 (RTF) を含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RTF_COMPRESSED  <br/> |
|識別子:  <br/> |0x1009  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |電子メール  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティと同じメッセージテキストが含まれていますが、RTF になっています。 
  
RTF 形式のメッセージテキストは、通常、圧縮形式で保存されます。 ただし、一部のシステムでは、書式設定されたテキストは圧縮されません。 これらに対応するために、MAPI では、ストリームヘッダーの dwMagicUncompressedRTF 値を使用して非圧縮 RTF を識別し、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) でメッセージの**STORE_UNCOMPRESSED_RTF**フラグを指定しています。保存非圧縮 RTF を格納できることを示します。 
  
このプロパティの内容を取得するには、 **openproperty**を呼び出してから、 **MAPI_READ**フラグを使用して[WrapCompressedRTFStream](wrapcompressedrtfstream.md)を呼び出します。 このプロパティに書き込むには、 **MAPI_MODIFY**および**MAPI_CREATE**フラグを使用してファイルを開きます。 これにより、新しいデータが古いデータに完全に置き換えられるようになり、ストアの更新の最小数を使用して書き込みが実行されます。 
  
RTF をサポートするメッセージストアは、メッセージテキストの空白への変更を無視します。 **PR_BODY**が初めて保存されると、メッセージストアはこのプロパティを生成して保存します。 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され、 **PR_BODY**が変更されている場合、メッセージストアは[rtfsync](rtfsync.md)関数を呼び出して RTF バージョンとの同期を確実に行います。 空白のみが変更された場合、プロパティは変更されません。 これにより、メッセージが rtf に対応していないクライアントおよびメッセージングシステムを経由するときに、重要な RTF 形式がすべて保持されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> 圧縮されたストリームを RTF メッセージの本文でエンコードおよびデコードします。
    
[[OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> メッセージと添付ファイルの RTF 本文のプロパティ内に、HTML などの追加のコンテンツ形式をカプセル化します。
    
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

