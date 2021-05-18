---
title: 自動構成のための新しいドメインの登録について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlookは、自動構成用の新しいメッセージ サービス ドメインを指定し、メッセージ サービス プロバイダーがアカウントを構成する方法を提供します。
ms.openlocfilehash: bf06ff8d145ed6173e3545f784f8b5b7b5f433be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316969"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>自動構成のための新しいドメインの登録について

Outlookは、自動構成用の新しいメッセージ サービス ドメインを指定し、メッセージ サービス プロバイダーがアカウントを構成する方法を提供します。
  
メッセージ サービス プロバイダーを設計するときに、Windows レジストリの次のキーを使用して、対応するメッセージ サービス プロバイダーによって自動的に構成される新しいドメインを指定できます。 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
キーでは、 `<domain name>` 自動構成のドメインです。 このドメイン名は、先頭でのみ \* ワイルドカードをサポートします。 次の表に、このキーでサポートされる値を示します。 
  
| 値 | 型 | 説明 |
|:-----|:-----|:-----|
|フレンドリ名  <br/> |REG_SZ  <br/> |自動構成時にユーザーに表示されるドメイン名。  <br/> |
|サービス名  <br/> |REG_SZ  <br/> |このドメインをサポートする mapisvc.inf に登録されているメッセージ サービス。  <br/> |
|インストール場所  <br/> |REG_SZ  <br/> |メッセージ サービス プロバイダーをインストールする場所の URL (まだインストールされていない場合)。  <br/> |
|最小バージョン  <br/> |REG_DWORD  <br/> |必要なメッセージ サービス .dllの最小バージョン。 この値は省略できます。  <br/> |
   
電子Outlookアカウントの自動構成を開始すると、電子メール アドレスで指定されたドメインWindowsレジストリがチェックされます。 ドメインがレジストリで既に指定されているWindows、メッセージ Outlook Mapisvc.inf に登録されているかどうかを確認します。 Outlookレジストリでドメインが指定されていない限り、ドメインの自動構成Windowsできません。
  
指定したメッセージ サービスが Mapisvc.inf に現在登録されていない場合、またはメッセージ サービス プロバイダーがインストールされているが、.dll のバージョンが指定した最小値より前の場合、Outlook は指定された表示名を使用して、プロバイダーのインストールを求めるプロンプトを表示します。 ユーザーが同意する場合Outlookプロバイダーをインストールできるよう、ユーザーを指定したインストール場所にリダイレクトします。 プロバイダーをインストールすると、Mapisvc.inf にメッセージ サービスが登録されます。
  
メッセージ サービスが現在 Mapisvc.inf に登録され、サービス プロバイダー .dll が適切なバージョンである場合、Outlook は[IMsgServiceAdmin::CreateMsgService](https://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)を使用してメッセージ サービスを作成し[、IMsgServiceAdmin::ConfigureMsgService](https://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx)を使用してメッセージ サービスを構成します。 Outlook構成では、次の 3 つのプロパティを使用して、プロバイダーがアカウントを設定できます[。PidTagAutoConfigurationUserName、PidTagAutoConfigurationUserEmail、](https://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)および[PidTagAutoConfigurationUserPassword](https://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx)です。 [](https://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx)
  
## <a name="see-also"></a>関連項目

- [MapiSvc.inf のファイル形式](https://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

