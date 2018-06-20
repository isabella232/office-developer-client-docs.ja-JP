---
title: PidTagServiceSupportFiles の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803568"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>PidTagServiceSupportFiles の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ サービスに属しているファイルの一覧が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SERVICE_SUPPORT_FILES、PR_SERVICE_SUPPORT_FILES_A、PR_SERVICE_SUPPORT_FILES_W  <br/> |
|識別子:  <br/> |0x3D0F  <br/> |
|データを入力します。  <br/> |PT_MV_STRING8、PT_MV_UNICODE  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>備考

[コントロール パネル] ダイアログ ボックスを使用すると、ユーザーはメッセージ サービスに属しているファイルの一覧を取得できます。 たとえば、ユーザーはサービスに属しているすべてのダイナミック リンク ライブラリ (Dll) の名前を取得できます。 ユーザーは、名前とすべての Dll のバージョン番号など、指定したファイルに関する追加情報をシークし、できます。 MAPI を使用して、これらのメッセージング ユーザーの選択ダイアログ ボックスにサポート ファイルの一覧を作成するプロパティです。
  
MAPI は、ファイル名でのみ動作し、Active Directory サービス インターフェイス (ANSI) 文字セットで、その他の文字列が渡されます。 正規機器製造元 (OEM) 文字セットでファイル名を使用するクライアント アプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。
  
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

