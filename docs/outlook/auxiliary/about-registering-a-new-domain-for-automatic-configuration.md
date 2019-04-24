---
title: 自動構成のための新しいドメインの登録について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook では、自動構成用に新しいメッセージサービスドメインを指定し、メッセージサービスプロバイダーがアカウントを構成できるようにする方法を提供します。
ms.openlocfilehash: bf06ff8d145ed6173e3545f784f8b5b7b5f433be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316969"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>自動構成のための新しいドメインの登録について

Outlook では、自動構成用に新しいメッセージサービスドメインを指定し、メッセージサービスプロバイダーがアカウントを構成できるようにする方法を提供します。
  
メッセージサービスプロバイダーを設計する場合、Windows レジストリの次のキーを使用して、対応するメッセージサービスプロバイダーによって自動的に構成される新しいドメインを指定できます。 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
キーで、 `<domain name>`は自動構成のドメインです。 このドメイン名は、先頭\*のみにワイルドカードをサポートしています。 次の表に、このキーがサポートする値を示します。 
  
| 値 | 型 | 説明 |
|:-----|:-----|:-----|
|フレンドリ名  <br/> |REG_SZ  <br/> |自動構成時にユーザーに対して表示されるドメイン名。  <br/> |
|サービス名  <br/> |REG_SZ  <br/> |このドメインをサポートする mapisvc.inf に登録されているメッセージサービス。  <br/> |
|インストール先  <br/> |REG_SZ  <br/> |メッセージサービスプロバイダーがまだインストールされていない場合は、その場所の URL。  <br/> |
|最小バージョン  <br/> |REG_DWORD  <br/> |必要なメッセージサービスプロバイダーの .dll の最小バージョン。 この値は省略できます。  <br/> |
   
Outlook は、電子メールアカウントの自動構成を開始するときに、電子メールアドレスによって指定されたドメインの登録を Windows レジストリで確認します。 ドメインが Windows レジストリで既に指定されている場合、Outlook はメッセージサービスが mapisvc.inf に登録されているかどうかを確認します。 Windows レジストリで指定されていない場合、Outlook はドメインの自動構成を続行できません。
  
指定されたメッセージサービスが mapisvc.inf に現在登録されていない場合、またはメッセージサービスプロバイダーがインストールされているが、.dll に指定されている最小値より前のバージョンがある場合、Outlook は指定されたフレンドリ名を使用して、ユーザーに供給. ユーザーが受け入れた場合、Outlook はユーザーがプロバイダーをインストールできるように、指定されたインストール場所にユーザーをリダイレクトします。 プロバイダーをインストールすると、mapisvc.inf にメッセージサービスが登録されます。
  
メッセージサービスが mapisvc.inf に現在登録されていて、サービスプロバイダが適切なバージョンである場合、Outlook は[IMsgServiceAdmin:: CreateMsgService](https://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)を使用してメッセージサービスを作成し、それを使用[して構成します。IMsgServiceAdmin:: ConfigureMsgService](https://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx)。 Outlook の自動構成では、次の3つのプロパティを使用して、プロバイダーがアカウントをセットアップできるようにします。 [PidTagAutoConfigurationUserName](https://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx)、 [PidTagAutoConfigurationUserEmail](https://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)、および[PidTagAutoConfigurationUserPassword](https://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>関連項目

- [mapisvc.inf のファイル形式](https://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

