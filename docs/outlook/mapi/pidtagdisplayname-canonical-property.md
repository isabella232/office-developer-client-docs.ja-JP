---
title: PidTagDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d914d071d0845dee7d402e45d281cd774095a5a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802718"
---
# <a name="pidtagdisplayname-canonical-property"></a>PidTagDisplayName 標準プロパティ

  
  
**適用対象**: Outlook 
  
特定の MAPI オブジェクトの表示名が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_NAME、PR_DISPLAY_NAME_A、PR_DISPLAY_NAME_W  <br/> |
|識別子:  <br/> |0x3001  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |一般的な MAPI  <br/> |
   
## <a name="remarks"></a>注釈

フォルダーには、一意の表示名を持つ兄弟のサブフォルダーが必要です。 などのフォルダーに 2 つのサブフォルダーが含まれている場合 2 つのサブフォルダーが同じ値をこのプロパティに使用することはできません。 この制限は、アドレス帳および配布リストなど、他のコンテナーには適用されません。 
  
サービス プロバイダーは、プロバイダーの種類と構成の情報が含まれるように、このプロパティの値を設定する必要があります。 その他の情報は、同じ種類のプロバイダーのインスタンスを区別するのに役立ちます。 未構成のプロバイダーは、プロバイダーの名前を示す文字列を使用してください。 構成済みのプロバイダーでは、かっこで囲まれた識別用の文字列の後に同じ文字列を使用してください。 などの構成解除状態のメッセージ ストア プロバイダーはこれらのプロパティを設定可能性があります。 
  
個人用インフォメーション ストア
  
構成済みのバージョンこれらのプロパティを設定し、でした。 
  
個人用インフォメーション ストア (1998 年 2 月 6 日)
  
状態のオブジェクトに対してこれらのプロパティには、ユーザー インターフェイスで表示可能なコンポーネントの名前が含まれています。 
  
> [!NOTE]
> MAPI メッセージの受信者の名前には、セミコロンを使用できません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダーの操作を処理します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
[[MS XWDVSEC]](http://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> 要求し、WebDAV メソッドを使用して Exchange のセキュリティ記述子を設定する方法を指定する WebDAV プロトコルを拡張します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagTransmittableDisplayName 標準プロパティ](pidtagtransmittabledisplayname-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

