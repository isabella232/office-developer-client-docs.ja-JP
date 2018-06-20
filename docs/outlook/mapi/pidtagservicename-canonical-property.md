---
title: PidTagServiceName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 260a35af11b76b1867c693723c1a7fa8133082fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803536"
---
# <a name="pidtagservicename-canonical-property"></a>PidTagServiceName の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
MapiSvc.inf ファイルのユーザーによって設定されたメッセージ サービスの名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SERVICE_NAME、PR_SERVICE_NAME_A、PR_SERVICE_NAME_W  <br/> |
|識別子:  <br/> |0x3D09  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティに含まれている名前は、メッセージ サービスに固有です。 MapiSvc.inf の [サービス] セクションからなります。
  
これらのプロパティは、メッセージ サービス テーブル内の列として表示され、サービスをフィルター処理に使用することができます。 サービスを特定するためには、値をローカライズしない必要があります。
  
## <a name="related-resources"></a>関連リソース

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

