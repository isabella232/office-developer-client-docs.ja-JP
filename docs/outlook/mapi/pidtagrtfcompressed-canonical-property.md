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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3091a76a1b755bf5a0d641ed9bd79bcfaa4641b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357891"
---
# <a name="pidtagrtfcompressed-canonical-property"></a>PidTagRtfCompressed 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リッチ テキスト形式 (RTF) バージョンのメッセージ テキスト (通常は圧縮形式) が含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RTF_COMPRESSED  <br/> |
|識別子:  <br/> |0x1009  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、RTF の PR_BODY **(** [PidTagBody](pidtagbody-canonical-property.md)) プロパティと同じメッセージ テキストが含まれる。 
  
RTF のメッセージ テキストは、通常、圧縮形式で保存されます。 ただし、一部のシステムでは書式設定されたテキストが圧縮されない場合があります。 MAPI には、非圧縮 RTF を識別するためのストリーム ヘッダーの dwMagicUncompressedRTF 値と、非圧縮 RTF を格納できるメッセージ ストアを示す **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) の **STORE_UNCOMPRESSED_RTF** フラグが提供されます。 
  
このプロパティの内容を取得するには **、OpenProperty** を呼び出し [、WrapCompressedRTFStream](wrapcompressedrtfstream.md) を呼び出 **MAPI_READ** します。 このプロパティに書き込むには、このプロパティを開き、MAPI_MODIFY **フラグMAPI_CREATE****します。** これにより、新しいデータが古いデータを完全に置き換え、ストア更新プログラムの最小数を使用して書き込みを実行できます。 
  
RTF をサポートするメッセージ ストアは、メッセージ テキスト内の空白への変更を無視します。 この **PR_BODY** が初めて格納される場合、メッセージ ストアは、このプロパティを生成して格納します。 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出され **、PR_BODY** が変更された場合、メッセージ ストアは [RTFSync](rtfsync.md)関数を呼び出して RTF バージョンとの同期を確認します。 空白だけが変更された場合、プロパティは変更されません。 これにより、メッセージが RTF 対応以外のクライアントおよびメッセージング システムを通過する際に、トリビアル以外の RTF 書式が保持されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXRTFCP]](https://msdn.microsoft.com/library/65dfe2df-1b69-43fc-8ebd-21819a7463fb%28Office.15%29.aspx)
  
> RTF メッセージのボディで圧縮ストリームをエンコードおよびデコードします。
    
[[MS-OXRTFEX]](https://msdn.microsoft.com/library/411d0d58-49f7-496c-b8c3-5859b045f6cf%28Office.15%29.aspx)
  
> メッセージと添付ファイルの RTF 本文プロパティ内に追加のコンテンツ形式 (HTML など) をカプセル化します。
    
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

