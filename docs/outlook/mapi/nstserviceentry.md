---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d68efa728b2cd62aca4ffbce02d2ea894ff74c35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595638"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
PST ベースのローカル ストアを NST ストアとしてラップする MAPI ストア プロバイダーのメッセージ サービス エントリ ポイント関数。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|実装元:  <br/> |MAPI プロバイダー  <br/> |
|呼び出し元:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a>パラメーター

 **NSTServiceEntry** は **[、MSGSERVICEENTRY 関数プロトタイプを](msgserviceentry.md)** 使用します。 パラメーターの詳細については **[、「MSGSERVICEENTRY」を参照してください](msgserviceentry.md)**。 
  
## <a name="return-values"></a>戻り値

戻り値の詳細については **[、「MSGSERVICEENTRY」を参照してください](msgserviceentry.md)**。 
  
## <a name="remarks"></a>注釈

**[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** を使用して msmapi32.dll でこの関数のアドレスを検索する場合は、プロシージャ名として "NSTServiceEntry" を指定します。 
  
レプリケーション API を使用するには、MAPI ストア プロバイダーが最初に **[NSTServiceEntry](nstserviceentry.md)** を呼び出して PST ベースのローカル ストアを開いてラップする必要があります。 プロバイダーは **[、API、IOSTX、IPSTX](iostxiunknown.md)** の主要なインターフェイス **[](ipstxiunknown.md)** を使用してレプリケーションを実行できます。 
  
次の注釈は、NST ストアに適用されます。
  
- **NSTServiceEntry** を使用する MAPI プロバイダーを実装する場合は、グローバル プロファイル セクションに情報を保存しない。 グローバル プロファイル セクションは多くのプロバイダーによって共有され、このプロファイルに格納されているデータは上書きできます。 
    
- 既存の変更タイム スタンプを持つアイテムだけが、保存時にスタンプを更新します。 
    
- アイテムを保存しても、競合チェックは自動的には行われません。
    
-  アイテムを保存しても重複検出は発生しません。 
    
-  キャッシュされたバージョンのサーバーを表すファイルが追加されます。NST。 
    
- グローバル プロファイル セクションへのポインターを取得するには、メッセージ サービスは、以下で定義されている **pbNSTGlobalProfileSectionGuid** を使用して、サポート オブジェクトで **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** を呼び出します。 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- この場合、メッセージ サービスのサポート オブジェクトは **、IMAPISupport::OpenProfileSection** が既定のプロファイル セクションの **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** プロパティで識別されるプロファイル セクションを返す必要があります。 このプロファイル セクションを取得するには、サポート オブジェクトで既定のプロファイル セクションを開き **、PR_SERVICE_UID** を取得し、その結果を **IMAPISupport::OpenProfileSection** に渡して、正しいグローバル プロファイル セクションを取得できます。 サポート オブジェクトは、このグローバル プロファイル セクションへのポインターをメッセージ サービスに返します。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)

