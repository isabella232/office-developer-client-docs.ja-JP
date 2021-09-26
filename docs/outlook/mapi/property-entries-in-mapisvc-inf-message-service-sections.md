---
title: MapiSvc.inf メッセージ サービス セクションのプロパティ エントリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8b6028e3c15f9c42f2fc8ad5672546d7fcf66b20
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599236"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>MapiSvc.inf メッセージ サービス セクションのプロパティ エントリ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティを設定するエントリでは、次の形式を使用します。
  
 **プロパティ タグ** **=** プロパティ値 
  
構成データが MAPI によって事前定義されたプロパティの 1 つを表す場合、またはデータが MAPI プロパティを表していない場合は標準以外のタグを表す場合、プロパティ タグには標準の MAPI プロパティ タグを指定できます。 標準以外のタグは、プロパティ識別子の値とプロパティの種類を組み合わせて作成されます。 結果は 8 桁の 16 進数です。 プロパティの値は、プロパティ タグに対して意味のある値を指定できます。 
  
メッセージ サービス セクションには、構成するメッセージ サービスに応じて、さまざまなエントリを含めできます。 通常、次の MAPI プロパティは、一覧表示された形式のメッセージ サービス セクションに含まれます。
  
 **PR_DISPLAY_NAME**  =  _string_
  
 **PR_SERVICE_DLL_NAME**  =  _DLL ファイルの名前_
  
 **PR_SERVICE_ENTRY_NAME**  =  _エントリ ポイント関数の名前_
  
 **PR_SERVICE_SUPPORT_FILES**  =  _ファイルの一覧_
  
 **PR_SERVICE_DELETE_FILES**  =  _ファイルの一覧_
  
 **PR_RESOURCE_FLAGS**  =  _ビットマスク_
  
PR_DISPLAY_NAME  ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 文字列は、ユーザー インターフェイスに表示されるメッセージ サービスの名前、ユーザーがメッセージ サービスに関連付ける名前です。 表示名は mapisvc.inf の省略可能なエントリです。 表示名が 2 つの部分で構成される場合があります。メッセージ サービスによって割り当てられたパーツと、ユーザーによって割り当てられたパーツ。 ユーザーがパーツの 1 つを割り当てる責任がある場合、これは通常、クライアント アプリケーションの制御下でメッセージ サービスによって提供されるプロパティ シートと呼ばれる特別なダイアログ ボックスで処理されます。 
  
メッセージ サービス ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))**エントリPR_SERVICE_DLL_NAME情報** は、メッセージ サービスを含む DLL の名前です。 **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) エントリに対して提供される情報は、MAPI がメッセージ サービスを構成するために呼び出す DLL 内のエントリ ポイント関数の名前です。 
  
メッセージ サービス ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))**エントリにPR_SERVICE_SUPPORT_FILES** ファイルは、メッセージ サービスと一緒にインストールする必要があるファイルです。 同様に、メッセージ サービスが **削除PR_SERVICE_DELETE_FILES、** メッセージ サービス ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) エントリ内のファイルを削除する必要があります。 
  
この **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) エントリは、メッセージ サービスに対して定義されたオプションのコレクションです。 たとえば、メッセージ サービスSERVICE_SINGLE_COPY特定のプロファイルに 1 回しか表示されない場合に、このビットが設定されます。 メッセージ SERVICE_NO_PRIMARY_IDENTITY ID 情報を提供しない場合は、このビットが設定されます。 
  
標準以外のプロパティ エントリの 2 つの例を次に示します。 最初のエントリは、既定のアドレス帳でプロパティ値として使用されるファイルへのパスを指定します。2 番目のエントリは、数値プロパティ値を指定します。 どちらのエントリも、AB メッセージ サービスに固有の意味を持ちます。
  
```cpp
6600001e=full path to file
66040003=integer

```


