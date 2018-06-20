---
title: PidTagViewDescriptorName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 9a186af55a8a2846bbb8af9e51be45ef73ce5d66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803662"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a>PidTagViewDescriptorName の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ビュー記述子の名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_VD_NAME、PR_VD_NAME_A、PR_VD_NAME_W  <br/> |
|識別子:  <br/> |0x7006  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |クラスによって定義されたメッセージ送信できます。  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、ビューの定義を含むフォルダーに関連付ける情報 (FAI) メッセージの空でない文字列に設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> 場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。
    
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

