---
title: PidTagServiceDllName の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 54fe624c98ddb631326853f387372468a61b2f70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803535"
---
# <a name="pidtagservicedllname-canonical-property"></a>PidTagServiceDllName の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
構成にするのにはメッセージ サービス プロバイダーのエントリ ポイント関数を含む DLL のファイル名が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SERVICE_DLL_NAME、PR_SERVICE_DLL_NAME_A、PR_SERVICE_DLL_NAME_W  <br/> |
|識別子:  <br/> |0x3D0A  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>備考

**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) メソッドのエントリ ポイント関数名が表示されたら、エントリ ポイントが存在することを示します。
  
MAPI は、DLL ファイルの名前付け規則を使用します。 ベース ファイル名には、DLL を一意に識別する最大 6 つの文字が含まれています。 MAPI では、32 ビット プラットフォーム上で動作するバージョンを識別する基本の DLL の名前に 32 の文字列を追加します。 たとえば、MAPI の名前です。DLL を指定すると、MAPI が MAPI32 名を作成します。DLL が、DLL の対応する 32 ビット バージョンを表す。
  
これらのプロパティは、基本名を指定する必要があります。 MAPI では、必要に応じて文字列の 32 を追加します。 エラーでこれらのプロパティの結果の一部として 32 の文字列を含みます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagProviderDllName の標準的なプロパティ](pidtagproviderdllname-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

