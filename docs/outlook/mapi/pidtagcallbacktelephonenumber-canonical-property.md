---
title: PidTagCallbackTelephoneNumber の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCallbackTelephoneNumber
api_type:
- HeaderDef
ms.assetid: e78d7e65-23a4-4359-b057-e06131cabf25
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c5764ea39af7a96a1bc6e6abfcbc29cc315adeda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802561"
---
# <a name="pidtagcallbacktelephonenumber-canonical-property"></a>PidTagCallbackTelephoneNumber の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージの受信者が送信者に到達するために使用できる電話番号が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CALLBACK_TELEPHONE_NUMBER、PR_CALLBACK_TELEPHONE_NUMBER_A、PR_CALLBACK_TELEPHONE_NUMBER_W  <br/> |
|識別子:  <br/> |0x3A02  <br/> |
|データを入力します。  <br/> |PT_UNICODE、PT_STRING8  <br/> |
|領域:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティでは、id、および受信者に関する情報にアクセスを提供するプロパティの例を示します。 受信者と受信者の組織によって定義されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先と個人用配布リスト オブジェクトの許可の操作を指定します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
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

