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
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360803"
---
# <a name="pidtagdisplayname-canonical-property"></a>PidTagDisplayName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した MAPI オブジェクトの表示名を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_NAME、PR_DISPLAY_NAME_A、PR_DISPLAY_NAME_W  <br/> |
|識別子:  <br/> |0x3001  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI 共通  <br/> |
   
## <a name="remarks"></a>解説

フォルダーには、一意の表示名を持つ兄弟サブフォルダーが必要です。 たとえば、フォルダーに2つのサブフォルダーが含まれている場合、2つのサブフォルダーでこのプロパティに同じ値を使用することはできません。 この制限は、アドレス帳や配布リストなど、他のコンテナーには適用されません。 
  
プロバイダーの種類と構成情報の両方が含まれるように、サービスプロバイダーはこのプロパティの値を設定する必要があります。 追加情報は、同じ種類のプロバイダーのインスタンスを区別するのに役に立ちます。 構成されていないプロバイダーは、プロバイダーの名前を示す文字列を使用する必要があります。 構成されたプロバイダーは、同じ文字列の後にかっこで囲んだ文字列を使用する必要があります。 たとえば、未構成のメッセージストアプロバイダーは、次のようなプロパティを設定することがあります。 
  
個人情報ストア
  
構成されたバージョンは、次のようにこれらのプロパティを設定できます。 
  
個人情報ストア (1998 年2月6日)
  
状態オブジェクトの場合、これらのプロパティには、ユーザーインターフェイスで表示できるコンポーネントの名前が含まれています。 
  
> [!NOTE]
> MAPI メッセージングでは、受信者名の中でセミコロンを使用することはできません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> webdav メソッドを使用して、Exchange セキュリティ記述子を要求および設定する方法を指定する webdav プロトコルを拡張します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagTransmittableDisplayName 標準プロパティ](pidtagtransmittabledisplayname-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

