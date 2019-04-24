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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339327"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>PidTagAttachLongFilename 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルの長いファイル名と拡張子を含みます (パスを除く)。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_LONG_FILENAME、PR_ATTACH_LONG_FILENAME_A、PR_ATTACH_LONG_FILENAME_W  <br/> |
|識別子:  <br/> |0x3707  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、 **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティの ATTACH_BY_VALUE、ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、および ATTACH_BY_REF_ONLY の各値に関連しています。 長いファイル名をサポートするプラットフォームは、送信時に**PR_ATTACH_LONG_FILENAME**プロパティと**PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) プロパティの両方を設定する必要があります。また、 **PR_ATTACH_LONG_FILENAME** first when をチェックする必要があります。いう. 
  
クライアントアプリケーションは、メッセージを受信するホストコンピューターが長いファイル名をサポートしている場合に、このプロパティに推奨される長いファイル名を設定する必要があります。 **PR_ATTACH_LONG_FILENAME**は、添付ファイルを保存するためのファイル名として使用でき、 **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティが指定されていない場合は、ファイル拡張子を指定します。 
  
**PR_ATTACH_FILENAME**によって提供されるファイル名とは異なり、この名前は8文字のファイル名に加えて、3文字の拡張子に制限されません。 その代わりに、ファイル名、内線番号、区切り期間など、最大256文字の長さを指定できます。 
  
MAPI は、ANSI 文字セットのファイル名に対してのみ機能します。 OEM 文字セットでファイル名を使用するクライアントアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
[[OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限が管理されたエンコード済みメッセージのプロパティを指定します。
    
[[OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> ボイスメールおよび fax メッセージを表すために許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mmapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

