---
title: PidLidAddressBookProviderArrayType の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3515d0f751cb6d8d0d427079691456519bac97dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801709"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>PidLidAddressBookProviderArrayType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
連絡先の電子メール アドレスの状態を指定して、ビット フラグのセットを表します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidABPArrayType  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008029  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>備考

**DispidABPArrayType**プロパティの値は、連絡先オブジェクトの状態を指定するフラグの組み合わせである必要があります。 個々 のフラグは、次の表で指定されます。 このプロパティが設定されている場合、 **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) する必要がありますプロパティ、同様です。 互いに同期された 2 つのプロパティを保持する必要があります。 などの場合は**dispidABPArrayType**では、ビットが"0x00000001"が設定されて、 **dispidABPEmailList**の値のいずれかの必要があります"0x00000000"です。 
  
|**ビット**|**説明**|
|:-----|:-----|
|0x00000001  <br/> |連絡先の Email1 が定義されています。  <br/> |
|0x00000002  <br/> |連絡先の電子メール 2 が定義されています。  <br/> |
|0x00000004  <br/> |連絡先の電子メール 3 が定義されています。  <br/> |
|0x00000008  <br/> |連絡先の勤務先ファックスが定義されています。  <br/> |
|0x00000010  <br/> |連絡先の自宅の fax が定義されています。  <br/> |
|0x00000020  <br/> |連絡先のプライマリ fax が定義されています。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

