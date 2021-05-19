---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Sway URI スキームを使用して Sway アプリケーションを開き、Sway を表示または編集します。
ms.openlocfilehash: 04848ef1de2777d916d8dd8dd381e6d5f66310d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415314"
---
# <a name="sway-uri-scheme"></a>Sway URI スキーム

このドキュメントでは、Sway アプリケーションの一様リソース識別子 (URI) の形式を定義Windows。 この URI スキームを使用して、さまざまなコマンドで Sway アプリケーションを呼び出します。

## <a name="sway-uri-scheme-syntax"></a>Sway URI スキームの構文

URI スキームの構文を次に示します。

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash;Sway が呼び出すアプリケーションを示します。 Sway for Windowsインストールされている場合は、Sway ハンドラー `ms-sway` Windowsに登録されます。
- `<command-argument>`URI には、アンパサンド ( ) 文字で区切られた 1 つ以上のコマンド &ndash; 引数 `&` が含まれています。 複数のコマンド引数が URI に含まれている場合、アンパサンド ( ) 文字は、各コマンド引数と次のコマンド引数 `&` を分離する必要があります。 コマンド引数はシナリオによって異なります。 

## <a name="command-arguments"></a>コマンド引数

Sway URL スキームの一部として、いくつかのコマンド引数を含めできます。 これらのコマンド引数は必須ではありません。 コマンド引数を含めない場合は、Sway アプリケーションが呼び出されます。

|コマンドの引数名|説明|型|可能な値|必須|
|:-----|:-----|:-----|:-----|:-----|
|**id**|Sway の一意の識別子。 開く Sway を示すために使用します。|String|Sway の有効な一意識別子。 ID は常に Sway の URL の一部です。<br/><br/>たとえば、次の Sway の `https://sway.com/dBheQgVZ1RQBfiQU` 場合、id は `dBheQgVZ1RQBfiQU` .<br/><br/>Sway アプリケーションに関連付けられているユーザー アカウントに編集権限がある場合、アプリケーションは編集モードで Sway を開きます。 それ以外の場合、アプリケーションはビュー モードで Sway を開きます。|いいえ|
|**mode**|編集用または表示用に、特定の Sway を開くモード。|String|edit<br/>view<br/><br/>**メモ**: id を **指定しない** 場合、このコマンド引数は無視されます。|いいえ|
|**auth_upn**|Sway を開く際に使用するアカウント。|String|有効な電子メール アドレス。<br/><br/>指定した電子メール アドレスが Sway アカウントに関連付けされていない場合、Sway はユーザーに指定したユーザーとしてサインインを求めるメッセージを表示します。<br/><br/>複数のアカウントが Sway アプリケーションに関連付けられている場合、指定した電子メール アドレスが存在する場合、Sway アプリケーションは呼び出されるとそのアカウントの使用に切り替わる。|いいえ|
|**auth \_ pvr**|Sway を開く場合に使用するアカウントの種類は、Microsoft アカウントまたは Azure Active Directory &mdash; アカウント (Azure AD)。|String|WindowsLiveId – **auth \_ upn** アカウントが Microsoft アカウントを指定します。<br/><br/>OrgId – **auth \_ upn** アカウントが Azure アカウントADします。<br/><br/>**auth \_ upn が指定されていない** 場合、このコマンド引数は無視されます。|いいえ|
|**アプリの \_ 呼び出し**|Sway を呼び出Windowsするアプリケーションの名前。|String|Sway URL スキームを介Windows呼び出しに使用される、アプリケーションの表示名です。<br/><br/>このコマンド引数の目的は、テレメトリと追跡です。|いいえ|

## <a name="uri-scheme-semantics"></a>URI スキームのセマンティクス

スキーム `<ms-sway>` は、Sway を開く場合や Sway アプリケーションを呼び出す際の URI 構文を定義します。 このスキームでは、いくつかのコマンド引数を定義します。この引数を使用して、次の操作を実行できます。 

- Sway アプリケーションを開 &ndash; く コマンド引数を指定する必要はありません。 

- Sway アプリケーションで表示する Sway を開く &ndash; 表示 **する ID** とモードセットを指定する必要があります。  

- Sway アプリケーションで編集用に Sway を開きます 編集する ID とモード &ndash; セットを指定する必要があります。   また、Sway を開く際に編集権限を持つ適切なアカウントが使用されるのを確認するために **、auth \_ upn** と **auth \_ pvr** も含める必要があります。  

## <a name="example"></a>例

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


