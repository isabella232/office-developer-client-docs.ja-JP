---
title: mapisvc.inf でのサービスおよびサービスプロバイダーの登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: '最終更新日: 2013 年7月18日'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328372"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>mapisvc.inf でのサービスおよびサービスプロバイダーの登録

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
システムに新しいプロバイダーをインストールするには、新しいプロバイダーをポイントするように mapisvc.inf ファイルを更新する必要があります。 構成中に設定される標準プロパティ。次のように、プロバイダーのダイナミックリンクライブラリ (.dll) を検索する場所を MAPI に通知します。
  
- **PR_SERVICE_DLL_NAME**は **[Message SERVICE]** セクションで指定されます。 
    
- **PR_PROVIDER_DLL_NAME**は **[サービスプロバイダ]** セクションで指定されます。 
    
> [!NOTE]
> プロバイダーの .dll の名前 (サフィックスが "32" なし) を設定することが想定されています。 その後、MAPI は、そのパスでプロバイダーを検索することによってプロバイダーを読み込みます。 
  
## <a name="putting-a-path-in-mapisvcinf"></a>mapisvc.inf にパスを配置する

ほとんどのアプリケーションは、プログラムファイルの下にインストールされます。 MAPI プロバイダーが動作するようにするには、path 変数を更新する必要があります。 いくつかの制限により、Microsoft outlook 2010 と outlook 2013 は MAPI プロバイダーへの完全なパスに対応できます。
  
mapisvc.inf にプロバイダーを登録する場合、MAPI プロパティ**PR_SERVICE_DLL_NAME**および**PR_PROVIDER_DLL_NAME**にプロバイダーへの完全なパスを含めることができます。
  
どちらのプロパティでも、ファイルを検索する前にファイル名に追加されたままになるので、完全なパスはサフィックスが "32" でなければなりません。 これは、"c:\mypath\myprovider.dll" というパスを登録すると、MAPI が "c:\mypath\myprovider32.dll" を読み込もうとすることを意味します。
  
Outlook の MAPI は完全なパスに対応するように設計されていないため、文字列の最初のピリオドを検索することによって、"32" サフィックスを挿入します。これは、他のピリオドを含むパスを使用できないため、次のようなパスは使用できません。"c:\my.path\myprovider.dll" または "c:\mypath\my.provider.dll"。
  
ストアプロバイダーでは、 **WrapStoreEntryID**関数を使用してエントリ識別子を生成することもあります。これは、プロバイダーの名前をパラメーターとして取ります。 
  
> [!IMPORTANT]
> mapisvc.inf で完全なパスを使用している場合は、 **WrapStoreEntryID**へのすべての呼び出しで同じパスを使用する必要があります。 
  
また、使用するパスは、 [getacp](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/)関数によって提供されるコードページを使用して、Unicode との間で変換される場合があります。 
  
> [!CAUTION]
> [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/)および[WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/)関数を使用して、このようなラウンドトリップを使用できない文字が含まれているパスを選択すると、エラーが発生します。 
  
この機能のデモを行うために、GitHub でラップされた[PST サンプル](https://github.com/stephenegriffin/Outlook2010CodeSamples)が改訂されました。関連する機能は**MergeWithMapiSvc**および**generateproviderpath**にあります。
  

