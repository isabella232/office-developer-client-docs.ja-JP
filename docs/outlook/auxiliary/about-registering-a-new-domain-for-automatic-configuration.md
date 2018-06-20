---
title: 自動構成の新しいドメインの登録について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook には、新しいメッセージ サービス用のドメインを自動構成を指定し、アカウントを構成するのにはメッセージ サービス プロバイダーを使用する方法が用意されています。
ms.openlocfilehash: c1daea81fe18e5d1088a233a3fcdff076419d6bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799301"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>自動構成の新しいドメインの登録について

Outlook には、新しいメッセージ サービス用のドメインを自動構成を指定し、アカウントを構成するのにはメッセージ サービス プロバイダーを使用する方法が用意されています。
  
メッセージ サービス プロバイダーを設計する場合は、対応するメッセージ サービス プロバイダーによって自動的に構成するのには新しいドメインを指定する Windows レジストリの次のキーを使用できます。 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
キーには、`<domain name>`は、ドメインを自動的に構成します。 このドメイン名は、ワイルドカードをサポートしています\*開始時のみです。 次の表は、このキーがサポートされている値を示します。 
  
| 値 | 種類 | 説明 |
|:-----|:-----|:-----|
|フレンドリ名  <br/> |REG_SZ  <br/> |自動構成中にユーザーに表示されているドメイン名です。  <br/> |
|サービス名  <br/> |REG_SZ  <br/> |メッセージ サービスは、このドメインをサポートしている mapisvc.inf に登録します。  <br/> |
|インストール場所  <br/> |REG_SZ  <br/> |インストールされていない場合、メッセージ ・ サービス ・ プロバイダーをインストールする場所の URL です。  <br/> |
|最小バージョン  <br/> |REG_DWORD  <br/> |必要なメッセージ ・ サービス ・ プロバイダーの .dll ファイルの最小バージョンです。 この値は省略可能です。  <br/> |
   
Outlook は、電子メール アカウントの自動構成を開始するときは、電子メール アドレスで指定されたドメインの登録のための Windows レジストリをチェックします。 ドメインは既に Windows のレジストリに指定されて、Outlook はメッセージ サービスが、Mapisvc.inf に登録されているかどうかをチェックします。 Outlook は、Windows レジストリで指定されていない限り、ドメインの自動構成を続行できません。
  
Outlook が指定したフレンドリ名を使用しをインストールするように求める場合 Mapisvc.inf に指定したメッセージ サービスが現在登録されていないか、メッセージ サービス プロバイダーがインストールされている .dll ファイルを指定された最小値より前のバージョンが、プロバイダーです。 ユーザーを受け取る場合、Outlook は、ユーザーがプロバイダーをインストールできるように、指定したインストール場所に、ユーザーをリダイレクトします。 Mapisvc.inf のメッセージ サービスを登録するプロバイダーをインストールします。
  
Outlook が[IMsgServiceAdmin::CreateMsgService](http://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)を使用して、メッセージ サービスを作成し、[を使用して構成し、メッセージ サービスは、現在登録されている Mapisvc.inf の場合、サービス プロバイダーの .dll ファイルは、適切なバージョンIMsgServiceAdmin::ConfigureMsgService](http://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx)。 Outlook の自動構成では、次の 3 つのプロパティを使用して、プロバイダーのアカウントを設定するを許可する: [PidTagAutoConfigurationUserName](http://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx)、 [PidTagAutoConfigurationUserEmail](http://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)、および[PidTagAutoConfigurationUserPassword](http://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>関連項目

- [MapiSvc.inf ファイルの形式](http://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

