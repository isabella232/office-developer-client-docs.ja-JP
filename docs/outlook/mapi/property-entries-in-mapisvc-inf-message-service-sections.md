---
title: MapiSvc.inf メッセージ サービス セクションのプロパティ エントリ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 038c13d24f3d797f7a4f8f9b7692240ce8004b74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580335"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a>MapiSvc.inf メッセージ サービス セクションのプロパティ エントリ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロパティを設定するエントリは、この形式を使用します。
  
 **プロパティ タグ****=** プロパティの値 
  
プロパティ タグは、データが MAPI プロパティを表していない場合の標準的な MAPI プロパティ タグの構成データを表している場合で MAPI では、定義済みのプロパティのいずれかまたは非標準のタグにあります。 非標準のタグがプロパティの型とプロパティの識別子の値を組み合わせることによって行われます。 8 桁の 16 進数になります。 プロパティ タグの意味は、どのようなプロパティを指定できます。 
  
メッセージ サービスのセクションでは、さまざまなエントリによって構成されているメッセージ サービスを含めることができます。 一覧の形式でメッセージのサービス] セクションでは、次の MAPI プロパティが含まれます通常。
  
 **PR_DISPLAY_NAME** =  _の文字列_
  
 **PR_SERVICE_DLL_NAME** =  _DLL ファイルの名前_
  
 **PR_SERVICE_ENTRY_NAME** =  _エントリ ポイント関数の名前_
  
 **PR_SERVICE_SUPPORT_FILES** =  _ファイルの一覧_
  
 **PR_SERVICE_DELETE_FILES** =  _ファイルの一覧_
  
 **PR_RESOURCE_FLAGS** =  _ビットマスク_
  
**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) の文字列は、ユーザーはメッセージ サービスに関連付けられた名前であり、ユーザー インターフェイスに表示されるメッセージ サービスの名前です。 表示名は、mapisvc.inf の省略可能なエントリです。 ふたつの部分表示名を作成する場合があります。メッセージ サービスによって割り当てられた部品と、ユーザーが割り当てられている部品です。 ユーザーが部品の 1 つの割り当てを担当する場合は、通常クライアント アプリケーションの制御下にあるメッセージ サービスによって提供されるプロパティ シートと呼ばれる特別なダイアログ ボックスで処理します。 
  
**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) のエントリの情報は、メッセージ サービスを含む DLL の名前です。 **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) のエントリの情報は、メッセージ サービスを構成するのには MAPI の呼び出しをその DLL 内のエントリ ポイント関数の名前です。 
  
**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) のエントリに記載されているファイルは、メッセージ サービスをインストールする必要があるファイルです。 同様に、メッセージ サービスが削除されたときは、 **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) のエントリ内のファイルを削除してください。 
  
**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のエントリは、メッセージ サービスに対して定義されているオプションの集合です。 たとえば、メッセージ サービスが一度だけ表示されます、特定のプロファイルの場合、SERVICE_SINGLE_COPY ビットが設定されます。 メッセージ サービスが id 情報を提供していない場合、SERVICE_NO_PRIMARY_IDENTITY ビットが設定されています。 
  
非標準のプロパティ エントリの 2 つの例に従います。 最初のエントリは、プロパティの値として既定のアドレス帳で使用されるファイルへのパスを指定します。2 番目のエントリでは、数値プロパティの値を指定します。 両方のエントリには、AB のメッセージ サービスに固有の意味があります。
  
```cpp
6600001e=full path to file
66040003=integer

```


