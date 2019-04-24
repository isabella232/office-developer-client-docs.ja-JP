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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280055"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI ストアプロバイダーのメッセージサービスエントリポイント関数。 PST ベースのローカルストアを NST ストアとしてラップします。 
  
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

 **nstserviceentry**は、 **[msgserviceentry](msgserviceentry.md)** 関数プロトタイプを使用します。 パラメーターの詳細については、「 **[msgserviceentry](msgserviceentry.md)**」を参照してください。 
  
## <a name="return-values"></a>戻り値

戻り値の詳細については、「 **[msgserviceentry](msgserviceentry.md)**」を参照してください。 
  
## <a name="remarks"></a>解説

**[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** を使用して msmapi32 でこの関数のアドレスを検索する場合は、プロシージャ名として "nstserviceentry" を指定します。 
  
レプリケーション API を使用するには、最初に**[nstserviceentry](nstserviceentry.md)** を呼び出して、MAPI ストアプロバイダーが PST ベースのローカルストアを開いてラップする必要があります。 プロバイダーは、API の主なインターフェイスである**[iostx](iostxiunknown.md)** と**[ipstx](ipstxiunknown.md)** を使用して、レプリケーションを実行することができます。 
  
次の解説は、NST ストアに適用されます。
  
- **nstserviceentry**を使用する MAPI プロバイダーを実装する場合は、[グローバルプロファイル] セクションに情報を格納しないでください。 [グローバルプロファイル] セクションは、多くのプロバイダーによって共有され、このプロファイルに格納されているデータは上書きできます。 
    
- 変更された既存のタイムスタンプを持つアイテムのみ、スタンプが保存されたときに更新されます。 
    
- アイテムが保存されるときに競合チェックは自動的に実行されません。
    
-  アイテムの保存時に重複データ検出が発生しません。 
    
-  サーバーのキャッシュされたバージョンを表すファイルがに追加されます。NST. 
    
- グローバルプロファイルセクションへのポインターを取得するために、メッセージサービスは、以下に定義されているように、 **pbNSTGlobalProfileSectionGuid**を使用して、support オブジェクトの**[imapisupport:: openprofile](imapisupport-openprofilesection.md)** セクションを呼び出します。 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- この場合、message service の support オブジェクトは、 **imapisupport:: openprofile** section が**[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** プロパティによって識別されるプロファイルセクションを既定のプロファイルセクションにあることを確認する必要があります。 このプロファイルセクションを取得するには、support オブジェクトで [既定のプロファイル] セクションを開き、 **PR_SERVICE_UID**を取得して、その結果を**imapisupport:: openprofile**セクションに渡すことで、適切なグローバルプロファイルセクションを取得できます。 このサポートオブジェクトは、メッセージサービスへのこのグローバルプロファイルセクションへのポインターを返します。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)

