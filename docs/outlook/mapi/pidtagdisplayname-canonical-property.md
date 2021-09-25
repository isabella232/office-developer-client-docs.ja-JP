---
title: PidTagDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c98d30e60bc88f11f3549ed7b76980677fea5f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555441"
---
# <a name="pidtagdisplayname-canonical-property"></a>PidTagDisplayName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の MAPI オブジェクトの表示名を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_NAME、PR_DISPLAY_NAME_A、PR_DISPLAY_NAME_W  <br/> |
|識別子:  <br/> |0x3001  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>注釈

フォルダーには、一意の表示名を持つ兄弟サブフォルダーが必要です。 たとえば、フォルダーに 2 つのサブフォルダーが含まれている場合、2 つのサブフォルダーでは、このプロパティに同じ値を使用できません。 この制限は、アドレス帳や配布リストなどの他のコンテナーには適用されません。 
  
サービス プロバイダーは、プロバイダーの種類と構成情報の両方を含むこのプロパティの値を設定する必要があります。 追加情報は、同じ種類のプロバイダーのインスタンスを区別するのに役立ちます。 構成されていないプロバイダーは、プロバイダーの名前を示す文字列を使用する必要があります。 構成済みのプロバイダーは、同じ文字列を使用し、その後にかっこで囲まれた識別文字列を使用する必要があります。 たとえば、構成されていないメッセージ ストア プロバイダーは、次のプロパティを設定できます。 
  
個人情報ストア
  
構成済みのバージョンでは、次のプロパティを次のように設定できます。 
  
個人情報ストア (1998 年 2 月 6 日)
  
状態オブジェクトの場合、これらのプロパティには、ユーザー インターフェイスで表示できるコンポーネントの名前が含まれます。 
  
> [!NOTE]
> MAPI メッセージングでは、受信者名内でセミコロンを使用できません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> WebDAV メソッドを使用してセキュリティ記述子を要求および設定する方法Exchange WebDAV プロトコルを拡張します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagTransmittableDisplayName 標準プロパティ](pidtagtransmittabledisplayname-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

