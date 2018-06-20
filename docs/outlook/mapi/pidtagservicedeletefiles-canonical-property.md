---
title: PidTagServiceDeleteFiles の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8f90d72e842df62c19c5aeeaf6c398c5db469560
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803544"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>PidTagServiceDeleteFiles の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ サービスのアンインストール時に削除するファイル名の一覧が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SERVICE_DELETE_FILES、PR_SERVICE_DELETE_FILES_A、PR_SERVICE_DELETE_FILES_W  <br/> |
|識別子:  <br/> |0x3D10  <br/> |
|データを入力します。  <br/> |PT_MV_STRING8、PT_MV_UNICODE  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>備考

メッセージ サービスをアンインストールするのには、コントロール パネルを使用する場合、これらのプロパティに含まれているボックスの一覧でファイル名がコンピューターから削除されます。 含めないでください、ボックスの一覧で複数のメッセージ サービスをサポートする任意の DLL または追加のメッセージ サービスを誤って削除された可能性があります。
  
MAPI は、ファイル名でのみ動作し、ANSI 文字セットで、その他の文字列が渡されます。 OEM 文字セットでファイル名を使用するアプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。
  
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

