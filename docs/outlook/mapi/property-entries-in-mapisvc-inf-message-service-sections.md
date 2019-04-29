---
title: mapisvc.inf メッセージサービスセクションのプロパティエントリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427998"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>mapisvc.inf メッセージサービスセクションのプロパティエントリ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティを設定するエントリは、次の形式を使用します。
  
 **プロパティタグ****=** プロパティ値 
  
構成データが mapi で定義されたプロパティの1つを表している場合、またはデータが mapi プロパティを表していない場合は標準でないタグとして、プロパティタグを標準の mapi プロパティタグにすることができます。 非標準のタグは、プロパティの識別子の値とプロパティの型を結合することによって作成されます。 結果は8桁の16進数値になります。 プロパティの値には、どのような意味でプロパティタグを指定できます。 
  
メッセージサービスセクションには、構成されているメッセージサービスに応じて、さまざまなエントリを含めることができます。 通常、次の MAPI プロパティは、表示されている形式のメッセージサービスセクションに含まれています。
  
 **PR_DISPLAY_NAME** =  _文字列_
  
 **** =  _DLL ファイルの PR_SERVICE_DLL_NAME 名_
  
 **** =  _エントリポイント関数の PR_SERVICE_ENTRY_NAME 名_
  
 **PR_SERVICE_SUPPORT_FILES** =  _ファイルの一覧_
  
 **PR_SERVICE_DELETE_FILES** =  _ファイルの一覧_
  
 **PR_RESOURCE_FLAGS** =  _ビットマスク_
  
**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 文字列は、ユーザーインターフェイスに表示されるメッセージサービスの名前です。これは、ユーザーがメッセージサービスと関連付けられます。 表示名は、mapisvc.inf の省略可能なエントリです。 表示名は2つの部分で構成される場合があります。メッセージサービスによって割り当てられたパーツと、ユーザーによって割り当てられたパーツ。 ユーザーがいずれかのパーツの割り当てを担当している場合は、通常、クライアントアプリケーションのコントロールの下に、メッセージサービスによって提供されるプロパティシートとして知られる特別なダイアログボックスで処理されます。 
  
**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) エントリに提供される情報は、メッセージサービスを含む DLL の名前です。 **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) エントリに提供されている情報は、MAPI がメッセージサービスを構成するために呼び出す DLL 内のエントリポイント関数の名前です。 
  
**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) エントリに記載されているファイルは、メッセージサービスと共にインストールする必要があります。 同様に、メッセージサービスが削除されたときに、 **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) エントリ内のファイルを削除する必要があります。 
  
**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) エントリは、メッセージサービスに対して定義されたオプションのコレクションです。 たとえば、SERVICE_SINGLE_COPY ビットは、メッセージサービスが特定のプロファイルに一度しか表示されない場合に設定されます。 メッセージサービスが id 情報を提供しない場合は、SERVICE_NO_PRIMARY_IDENTITY ビットが設定されます。 
  
標準的でないプロパティエントリの2つの例を次に示します。 最初のエントリは、プロパティ値として既定のアドレス帳で使用されるファイルへのパスを指定します。2番目のエントリは、数値プロパティ値を指定します。 両方のエントリが AB メッセージサービスに固有のものであることを意味します。
  
```cpp
6600001e=full path to file
66040003=integer

```


