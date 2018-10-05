---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392418"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI のメッセージ サービスのエントリ ポイントの関数では、NST ストアとして PST ベースのローカル ストアをラップするプロバイダーを格納します。 
  
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

 **NSTServiceEntry**は、 **[MSGSERVICEENTRY](msgserviceentry.md)** 関数のプロトタイプを使用します。 そのパラメーターについては、 **[MSGSERVICEENTRY](msgserviceentry.md)** を参照してください。 
  
## <a name="return-values"></a>戻り値

戻り値については、 **[MSGSERVICEENTRY](msgserviceentry.md)** を参照してください。 
  
## <a name="remarks"></a>備考

Msmapi32.dll のこの関数のアドレスを検索するには、 **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** を使用して、プロシージャ名として"NSTServiceEntry"を指定します。 
  
レプリケーション API を使用するには、MAPI ストア プロバイダーする必要があります最初を開き**[NSTServiceEntry](nstserviceentry.md)** を呼び出すことによって PST ベースのローカル ストアをラップします。 プロバイダーは、レプリケーションを実行するための API、 **[IOSTX](iostxiunknown.md)** **[IPSTX](ipstxiunknown.md)**、主要なインタ フェースを使用できます。 
  
NST ストアには、次の「解説」が適用されます。
  
- **NSTServiceEntry**を使用している MAPI プロバイダーを実装する場合は、グローバル プロファイル セクション内の情報を保存しないでください。 グローバル プロファイル セクションでは、多くのプロバイダーによって共有され、このプロファイルに格納されたデータが上書きされることができます。 
    
- 既存の変更のタイムスタンプを持つアイテムだけが保存されるときに更新のタイムスタンプを取得します。 
    
- 競合チェックは発生しません自動的にアイテムが保存されます。
    
-  重複データ検出は、アイテムが保存されたときに発生しません。 
    
-  サーバーのキャッシュされたバージョンを表すファイルが追加されます。NST です。 
    
- グローバル プロファイル セクションへのポインターを取得するには、メッセージ サービスは、下記のように**pbNSTGlobalProfileSectionGuid**を使用してサポート オブジェクトの**[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** を呼び出します。 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- この例では、メッセージ サービスのサポート オブジェクトは、 **IMAPISupport::OpenProfileSection**が既定のプロファイル セクション内の**[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** プロパティによって識別されるプロファイルのセクションを返すようにしてください。 サポート オブジェクトが既定のプロファイル セクションを開くことができますこのプロファイルのセクションを取得するには、 **PR_SERVICE_UID**を取得し、結果を適切なグローバル プロファイル セクションを取得するのには**IMAPISupport::OpenProfileSection**に渡します。 サポート オブジェクトは、メッセージ サービスには、このグローバル プロファイル セクションへのポインターを返します。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)

