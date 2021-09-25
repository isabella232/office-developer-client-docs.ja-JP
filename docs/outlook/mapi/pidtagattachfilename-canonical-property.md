---
title: PidTagAttachFilename 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fd3796c6c05055fd29953c01f1a6495e88342b5c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563876"
---
# <a name="pidtagattachfilename-canonical-property"></a>PidTagAttachFilename 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
パスを除く添付ファイルの基本ファイル名と拡張子が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_FILENAME、PR_ATTACH_FILENAME_A、PR_ATTACH_FILENAME_W  <br/> |
|識別子:  <br/> |0x3704  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

添付ファイル オブジェクトは **、PR_ATTACH_METHOD** **(** [PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの **ATTACH_BY_VALUE、ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、** および **ATTACH_BY_REF_ONLY** の値に関連するこれらのプロパティを公開をお勧めします。  **PR_ATTACH_FILENAME** 値を使用する場合は、プロパティと関連付けられたプロパティが必要です。 
  
これらのプロパティは **、PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティが指定されていない場合に、添付ファイルを保存し、ファイル名の拡張子を指定するために推奨されるファイル名として使用できます。 
  
ファイル名は、8 文字と 3 文字の拡張子に制限されます。 長いファイル名をサポートするプラットフォームの場合は、このプロパティと PR_ATTACH_LONG_FILENAME **(** [PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) プロパティの両方を設定します。 
  
MAPI は、ファイル名、およびファイルに渡されるその他の文字列 (ANSI) 文字セットでのみ動作します。 元の機器メーカー (OEM) の文字セットでファイル名を使用するクライアント アプリケーションは、MAPI を呼び出す前に ANSI に変換する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限で管理されたエンコードされたメッセージのプロパティを指定します。
    
[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> S/MIME 署名済みおよび暗号化されたメッセージのプロパティを指定します。
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。
    
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

