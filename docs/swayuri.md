---
title: swayuri
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: sway の URI スキームを使用して、sway アプリケーションを開き、sway を表示または編集します。
ms.openlocfilehash: 04848ef1de2777d916d8dd8dd381e6d5f66310d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415314"
---
# <a name="sway-uri-scheme"></a>Sway URI スキーム

このドキュメントでは、Windows 用 Sway アプリケーションの Uniform resource identifier (uri) の形式を定義します。 この URI スキームを使用すると、さまざまなコマンドを使用して Sway アプリケーションを呼び出すことができます。

## <a name="sway-uri-scheme-syntax"></a>Sway URI スキームの構文

URI スキームの構文は次のとおりです。

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Sway が起動するアプリケーションであることを示します。 windows がインストールされている`ms-sway`場合、sway ハンドラーとして windows に登録されます。
- `<command-argument>`&ndash; URI には、アンパサンド (`&`) 文字で区切られた1つ以上の command 引数を含めることができます。 URI に複数のコマンド引数が含まれている場合、アンパサンド (`&`) 文字は、次のコマンド引数と各コマンド引数を区切る必要があります。 Command 引数は、シナリオによって異なります。 

## <a name="command-arguments"></a>コマンド引数

Sway の URL スキームの一部として、いくつかのコマンド引数を含めることができます。 これらのコマンド引数は必須ではありません。 command 引数を指定しない場合は、Sway アプリケーションが呼び出されます。

|コマンド引数名|説明|型|可能な値|必須|
|:-----|:-----|:-----|:-----|:-----|
|**id**|Sway の一意の識別子。 開く Sway を示すために使用します。|String|Sway の有効な一意の識別子。 id は常に Sway への URL の一部です。<br/><br/>たとえば、次の Sway `https://sway.com/dBheQgVZ1RQBfiQU`の場合、id は`dBheQgVZ1RQBfiQU`です。<br/><br/>sway アプリケーションに関連付けられたユーザーアカウントに編集権限がある場合は、アプリケーションによって編集モードで sway が開かれます。 それ以外の場合、アプリケーションは、表示モードで Sway を開きます。|いいえ|
|**mode**|特定の Sway を開く必要があるモード。編集するか表示するかを指定します。|String|edit<br/>ビュー<br/><br/>**注**: **id**が指定されていない場合、このコマンド引数は無視されます。|いいえ|
|**auth_upn**|Sway を開くときに使用するアカウントです。|String|有効な電子メールアドレス。<br/><br/>指定した電子メールアドレスが sway アカウントに関連付けられていない場合、sway はユーザーに指定されたユーザーとしてサインインすることを要求します。<br/><br/>複数のアカウントが Sway アプリケーションに関連付けられていて、指定された電子メールアドレスが存在する場合、sway アプリケーションは起動時にそのアカウントを使用するように切り替わります。|いいえ|
|**auth\_pvr**|Sway&mdash;を開くために使用するアカウントの種類。 Microsoft アカウントまたは azure Active Directory アカウント (azure AD) のいずれかを開きます。|String|WindowsLiveId – **auth\_upn**アカウントが Microsoft アカウントであることを指定します。<br/><br/>orgid –**認証\_upn**アカウントが Azure AD アカウントであることを指定します。<br/><br/>**認証\_upn**が指定されていない場合、このコマンド引数は無視されます。|いいえ|
|**アプリ\_の起動**|Sway を起動するために使用する Windows アプリケーションの名前。|String|sway の URL スキーム経由で sway を呼び出すために使用される Windows アプリケーションのフレンドリ名。<br/><br/>このコマンド引数の目的は、テレメトリと追跡用です。|いいえ|

## <a name="uri-scheme-semantics"></a>URI スキームのセマンティクス

この`<ms-sway>`スキームは、sway を開くため、または sway アプリケーションを呼び出すための URI 構文を定義します。 このスキームでは、次の操作を実行するために使用できるいくつかのコマンド引数が定義されています。 

- Sway アプリケーション&ndash;を開くコマンド引数を指定する必要はありません。 

- sway アプリケーション&ndash;で表示する sway を開く**id**と**モード**を指定する必要があります。 

- sway アプリケーション&ndash;で sway を開いて編集するには、編集のために設定する**id**と**モード**を指定する必要があります。 Sway を開いたときに編集アクセス許可を持つ適切なアカウントが使用されるように、 **auth\_upn**と**auth\_pvr**を含めることをお勧めします。  

## <a name="example"></a>例

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


