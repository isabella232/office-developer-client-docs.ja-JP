---
title: PidTagServiceSupportFiles 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417043"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>PidTagServiceSupportFiles 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスに属するファイルの一覧を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SERVICE_SUPPORT_FILES、PR_SERVICE_SUPPORT_FILES_A、PR_SERVICE_SUPPORT_FILES_W  <br/> |
|識別子:  <br/> |0x3D0F  <br/> |
|データの種類 :   <br/> |PT_MV_STRING8、PT_MV_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>注釈

コントロール パネルアプレットのダイアログ ボックスを使用して、ユーザーはメッセージ サービスに属するファイルの一覧を取得できます。 たとえば、ユーザーは、サービスに属しているすべてのダイナミック リンク ライブラリ (DLL) の名前を取得できます。 その後、指定したファイルに関する詳細情報 (すべての DLL の名前やバージョン番号など) を検索できます。 MAPI では、これらのプロパティを使用して、メッセージング ユーザーの選択用のダイアログ ボックスにサポート ファイルの一覧を作成します。
  
MAPI は、Active Directory Service Interfaces (ANSI) 文字セット内のファイル名と、そのファイルに渡される他の文字列でのみ動作します。 元の機器メーカー (OEM) の文字セットでファイル名を使用するクライアント アプリケーションは、MAPI を呼び出す前に ANSI に変換する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

