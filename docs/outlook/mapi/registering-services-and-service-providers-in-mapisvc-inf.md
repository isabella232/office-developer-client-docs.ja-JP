---
title: MapiSvc.inf でのサービスおよびサービス プロバイダーの登録
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: '最終更新日: 2013 年 7 月 18 日'
ms.openlocfilehash: edb67fde04a3aa27713c3de47a9a0e7f01eb4b97
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399555"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>MapiSvc.inf でのサービスおよびサービス プロバイダーの登録

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
システムに新しいプロバイダーをインストールするには、新しいプロバイダーを指すように、MapiSvc.inf ファイルを更新する必要があります。 通知 MAPI プロバイダーのダイナミック リンク ライブラリ (.dll) を検索する場所の次のよう、標準のプロパティの構成中に設定します。
  
- **PR_SERVICE_DLL_NAME**は、 **[メッセージ サービス]** セクションで指定されます。 
    
- **PR_PROVIDER_DLL_NAME**は、 **[サービス プロバイダー]** セクションで指定されます。 
    
> [!NOTE]
> (32 のサフィックス) がない場合、プロバイダーの .dll の名前を設定することを予想にされます。 MAPI は、し、それを探すパス上で、プロバイダーを読み込みます。 
  
## <a name="putting-a-path-in-mapisvcinf"></a>MapiSvc.inf にパスを配置すること

[プログラム ファイル、MAPI プロバイダーが動作できるようにするのには path 変数の更新を必要とするほとんどのアプリケーションをインストールします。 制限がいくつかの Microsoft Outlook 2010、Outlook 2013 は、MAPI プロバイダーに完全なパスに対応できます。
  
MapiSvc.inf のプロバイダーを登録すると、ときに**PR_SERVICE_DLL_NAME**と**PR_PROVIDER_DLL_NAME**は、MAPI プロパティのプロバイダーの完全なパスを配置する可能性があります。
  
いずれかのプロパティの完全なパス必要がありますサフィックス 32、MAPI は、ファイルを検索する前にファイル名を追加し続けるため。 つまり"c:\mypath\myprovider.dll"のパスを登録する場合は、MAPI がしようとする"c:\mypath\myprovider32.dll"を読み込めません。
  
Outlook の完全なパスに対応するために MAPI が想定されていません、つまり、他のピリオドを含むパスでは使用できません、次のようにパスを使用することはできませんので、文字列の最初の期間を検索しながらなどの挿入が行われます"c:\my.path\myprovider.dll"または"c:\mypath\my.provider.dll"です。
  
ストア プロバイダーのプロバイダーの名前をパラメーターとして受け取り、 **WrapStoreEntryID**関数を使用してエントリの識別子が生成されます。 
  
> [!IMPORTANT]
> MapiSvc.inf の完全パスを使用する場合は、 **WrapStoreEntryID**への呼び出しで同じパスを使用する必要があります。 
  
さらに、 [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/)関数が用意されているコード ページを使用して Unicode との間に使用するパスを変換することがあります。 
  
> [!CAUTION]
> [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/)と[WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/)関数を使用して、このようなラウンドト リップに対応できない文字を含むパスを選択する場合、障害が発生します。 
  
この機能のデモでは、CodePlex で[ラップの PST のサンプル](https://ol2010mapisamples.codeplex.com/)が更新されました - **MergeWithMapiSvc**と**GenerateProviderPath**では、関連する機能です。
  

