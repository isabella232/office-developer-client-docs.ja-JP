---
title: PidTagServiceEntryName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceEntryName
api_type:
- COM
ms.assetid: 783f08aa-fb5a-432d-b8bd-48d69f0e5c38
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0d75616aaa6599709828d32393a316c642bc613b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803527"
---
# <a name="pidtagserviceentryname-canonical-property"></a>PidTagServiceEntryName の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ サービスの構成のエントリ ポイント関数の名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SERVICE_ENTRY_NAME  <br/> |
|識別子:  <br/> |0x3D0B  <br/> |
|データを入力します。  <br/> |PT_STRING8  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>備考

メッセージ サービスのエントリ ポイントを提供するメッセージ サービスの実装者が、エントリ ポイントが必要ではないことをお勧めします。 ただし、エントリ ポイントは、関連する設定のプロパティが存在する場合にのみ指定してください。 MAPI ではこれらのプロパティが存在しない場合、エントリ ポイントが指定されていないと見なされます。
  
**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) は、エントリ ポイント関数が入力されているダイナミック リンク ライブラリ (DLL) と呼びます。
  
メッセージ サービスのエントリ ポイントの詳細については、[サービス プロバイダーのエントリ ポイント関数を実装する](implementing-a-service-provider-entry-point-function.md)を参照してください。
  
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

