---
title: PidTagRtfCompressed の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c93d850551e766e97292d5417c3be5577f557af0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803382"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>PidTagRtfCompressed の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
リッチ テキスト形式 (RTF) バージョン圧縮形式では通常、メッセージのテキストにはが含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RTF_COMPRESSED  <br/> |
|識別子:  <br/> |0x1009  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>備考

このプロパティには、([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティとしては、rtf 形式では、同じメッセージ テキストが含まれています。 
  
Rtf 形式のメッセージのテキストは通常、圧縮形式で格納します。 ただし、いくつかのシステムでは、書式設定されたテキストは圧縮の操作を行います。 MAPI が圧縮されていない rtf 形式、およびメッセージの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) で、 **STORE_UNCOMPRESSED_RTF**フラグを指定するようにストリーム ヘッダーの dwMagicUncompressedRTF 値を提供する対応するためにを保存すると、非圧縮の rtf 形式を格納できることを示します。 
  
このプロパティの内容を取得するには、 **OpenProperty**を呼び出してから、 **MAPI_READ**フラグを使用して[WrapCompressedRTFStream](wrapcompressedrtfstream.md)をコールします。 このプロパティに書き込むには、 **MAPI_MODIFY**と**タグ**のフラグが設定されたことを開きます。 これにより、新しいデータは、古いデータを完全に置き換えるし、更新プログラムの格納の最小数を使用して書き込みを実行することです。 
  
RTF をサポートしているメッセージ ・ ストアは、メッセージのテキスト内の空白への変更を無視します。 **PR_BODY**が最初に保存されると、メッセージ ・ ストアによっても生成し、このプロパティを格納します。 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出された後で、 **PR_BODY**が変更された場合は、メッセージ ・ ストアは、rtf 形式のバージョンとの同期を確実に[行う](rtfsync.md)関数を呼び出します。 プロパティを左の空白が変更されているだけの場合そのままです。 これには、任意の複雑な RTF メッセージが RTF に対応していないクライアントを通過するときの書式を設定して、メッセージング システムが保持されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXRTFCP]](http://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> エンコードし、圧縮された RTF メッセージの本文のストリームをデコードします。
    
[[MS OXRTFEX]](http://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> 内のメッセージと添付ファイルの rtf 形式の本文のプロパティ (HTML) などの他のコンテンツ形式をカプセル化します。
    
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

