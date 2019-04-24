---
title: PidTagAttachFilename 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319223"
---
# <a name="pidtagattachfilename-canonical-property"></a>PidTagAttachFilename 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルの基本ファイル名と拡張子を含みます (パスを除く)。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_FILENAME、PR_ATTACH_FILENAME_A、PR_ATTACH_FILENAME_W  <br/> |
|識別子:  <br/> |0x3704  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>解説

attachment オブジェクトは、これらのプロパティを公開することをお勧めします。これらのプロパティは、 **PR_ATTACH_METHOD**の**ATTACH_BY_VALUE**、 **ATTACH_BY_REFERENCE**、 **ATTACH_BY_REF_RESOLVE**、および**ATTACH_BY_REF_ONLY**の値に関連しています。([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) プロパティ。 これらの値のいずれかを使用する場合は、 **PR_ATTACH_FILENAME**および関連するプロパティが必要です。 
  
これらのプロパティは、添付ファイルを保存するための推奨されるファイル名として使用でき、 **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) プロパティが指定されていない場合はファイル名拡張子を指定します。 
  
ファイル名が8文字に制限され、3文字の拡張子になります。 長いファイル名をサポートするプラットフォームでは、このプロパティと**PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) プロパティの両方を設定します。 
  
MAPI は、米国規格協会 (ANSI) 文字セットで、ファイル名とそれに渡されるその他の文字列に対してのみ機能します。 OEM (相手先ブランド供給) 文字セットでファイル名を使用するクライアントアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
[[OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> 権限が管理されたエンコード済みメッセージのプロパティを指定します。
    
[[OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> S/MIME で署名および暗号化されたメッセージのプロパティを指定します。
    
[[OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトをエンコードし、効率的なストリーム表現にデコードします。
    
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

