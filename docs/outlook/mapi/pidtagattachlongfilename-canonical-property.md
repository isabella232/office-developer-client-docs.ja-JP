---
title: PidTagAttachLongFilename 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339327"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>PidTagAttachLongFilename 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
パスを除く添付ファイルの長いファイル名と拡張子を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_LONG_FILENAME、PR_ATTACH_LONG_FILENAME_A、PR_ATTACH_LONG_FILENAME_W  <br/> |
|識別子:  <br/> |0x3707  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、ATTACH_BY_VALUE(PidTagAttachMethod) プロパティの ATTACH_BY_VALUE、ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、ATTACH_BY_REF_ONLY **PR_ATTACH_METHOD** の値に関連 [](pidtagattachmethod-canonical-property.md)します。 長いファイル **名** をサポートするプラットフォームでは、送信時に **PR_ATTACH_LONG_FILENAME** プロパティと **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) プロパティの両方を設定し、受信時に最初に PR_ATTACH_LONG_FILENAME を確認する必要があります。 
  
クライアント アプリケーションは、メッセージを受信するホスト コンピューターが長いファイル名をサポートしている場合に使用する推奨される長いファイル名にこのプロパティを設定する必要があります。 **PR_ATTACH_LONG_FILENAME** を保存するファイル名として使用し **、PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティが指定されていない場合は、ファイル名の拡張子を指定できます。 
  
PR_ATTACH_FILENAME によって提供 **されるファイル名** とは異なり、この名前は 8 文字のファイル名と 3 文字の拡張子に制限されません。 その代わりに、ファイル名、拡張子、区切り記号のピリオドを含む最大 256 文字の長い文字を指定できます。 
  
MAPI は、ANSI 文字セット内のファイル名でのみ動作します。 OEM 文字セットでファイル名を使用するクライアント アプリケーションは、MAPI を呼び出す前に ANSI に変換する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限で管理されたエンコードされたメッセージのプロパティを指定します。
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> ボイス メールおよび FAX メッセージを表す場合に許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mmapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

