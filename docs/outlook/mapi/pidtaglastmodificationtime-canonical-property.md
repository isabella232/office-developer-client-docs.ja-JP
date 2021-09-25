---
title: PidTagLastModificationTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a51a2c12c1c5609cf02ec4e19ed01dc4ae217328
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613395"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>PidTagLastModificationTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトまたはサブオブジェクトが最後に変更された日時を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|識別子:  <br/> |0x3008  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |メッセージ時刻  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、最初はプロパティ ([PidTagCreationTime](pidtagcreationtime-canonical-property.md) **)** プロパティPR_CREATION_TIME同じ値に設定されます。 添付ファイル サブオブジェクトは、ネイティブ ファイル システムによって保持された最後の変更時刻をコピーすることで、必要に応じて更新できます。 クライアント アプリケーションは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを最初に呼び出すまで、このプロパティを設定できます。 それ以降、プロバイダーは **IMAPIProp::SaveChanges** 呼び出 **し** PR_LAST_MODIFICATION_TIME間に更新する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアント間のメッセージング オブジェクト データの同期を処理します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
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

