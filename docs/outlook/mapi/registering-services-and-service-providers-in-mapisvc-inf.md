---
title: MapiSvc.inf でのサービスとサービス プロバイダーの登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: '最終更新日: 2013 年 7 月 18 日'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328372"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>MapiSvc.inf でのサービスとサービス プロバイダーの登録

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
システムに新しいプロバイダーをインストールするには、MapiSvc.inf ファイルを更新して新しいプロバイダーをポイントする必要があります。 構成時に設定される標準プロパティ (以下を含む) は、プロバイダーの動的リンク ライブラリを見つける場所を MAPI に通知します (.dll)。
  
- この **PR_SERVICE_DLL_NAME** [Message **Service] セクションで指定** します。 
    
- この **PR_PROVIDER_DLL_NAME** [サービス プロバイダー] **セクションで指定** します。 
    
> [!NOTE]
> 期待される点は、プロバイダーの名前を (サフィックス "32" .dll付けずに) 設定するということです。 MAPI は、パスでプロバイダーを探して、プロバイダーを読み込む。 
  
## <a name="putting-a-path-in-mapisvcinf"></a>MapiSvc.inf にパスを入れる

ほとんどのアプリケーションは Program Files の下にインストールされ、MAPI プロバイダーが動作するためにパス変数を更新する必要があります。 いくつかの制限により、Microsoft Outlook 2010 Outlook 2013 は MAPI プロバイダーへの完全なパスに対応できます。
  
MapiSvc.inf にプロバイダーを登録する場合は、MAPI プロパティおよび MAPI プロパティにプロバイダーへの完全なパスPR_SERVICE_DLL_NAME **置** PR_PROVIDER_DLL_NAME。
  
どちらのプロパティでも、MAPI はファイルを探す前にファイル名に追加し続けるので、完全パスには接尾辞 "32" を付けない必要があります。 つまり、"c:\mypath\myprovider.dll" パスを登録すると、MAPI は "c:\mypath\myprovider32.dll" を読み込c:\mypath\myprovider32.dll。
  
Outlook の MAPI はもともと完全なパスに対応するように設計されていたため、文字列の最初のピリオドを探して"32" サフィックスを挿入します。つまり、他の期間を含むパスは機能しないので、"c:\my.path\myprovider.dll" や "c:\mypath\my.provider.dll" などのパスを使用することはできません。
  
ストア プロバイダーでは **、WrapStoreEntryID** 関数を使用してエントリ識別子を生成し、プロバイダーの名前をパラメーターとして受け取る場合があります。 
  
> [!IMPORTANT]
> MapiSvc.inf でフル パスを使用している場合は **、WrapStoreEntryID** の呼び出しで同じパスを使用する必要があります。 
  
さらに [、GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) 関数によって提供されるコード ページを使用して、使用するパスを Unicode に変換して Unicode から変換することもできます。 
  
> [!CAUTION]
> [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/)関数と[WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/)関数を通じてこのようなラウンドトリップを生き残れない文字を含むパスを選択すると、エラーが発生します。 
  
この機能のデモンストレーションでは、GitHub のラップ [された PST](https://github.com/stephenegriffin/Outlook2010CodeSamples) サンプルが改訂されました。関連する機能は **MergeWithMapiSvc** および **GenerateProviderPath** にあります。
  

