---
title: ユーザー設定アイテム タイプの競合解決について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 3f0853fc-f9f2-4314-ac55-47fe1e52d019
description: このトピックでは、ユーザー設定で作成したカスタム アイテムの種類の競合を解決する方法Outlook。
ms.openlocfilehash: 357dd9182f26c4e9e1e264afdee296859e7b3483
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316948"
---
# <a name="about-conflict-resolution-for-custom-item-types"></a>ユーザー設定アイテム タイプの競合解決について

このトピックでは、ユーザー設定で作成したカスタム アイテムの種類の競合を解決する方法Outlook。
  
## <a name="conflict-resolution-for-standard-outlook-item-types"></a>標準のアイテムの種類の競合Outlook解決

このOutlook、同じアイテムの 2 つ以上のコピーが互いに独立して変更された場合に競合が発生します。 Outlookの間に競合を検出します。 たとえば、オフラインで作業するときに、Outlook Web Appで会議アイテムをオンラインで更新し、Outlookで同じ会議アイテムを更新できます。 クライアントOutlookオンラインに戻り、クライアント コンピューターとサーバーの間でデータを同期すると、同じ会議アイテムの 2 つの異なるコピーが検出されます。
  
標準Outlook Outlook アイテムの種類に属するアイテムを同期する場合、そのアイテムの種類に固有のプロパティを考慮して、競合の可能性を検出します。 Outlookの解決を試み、ユーザーの介入を要求せずに、結果のコピーを適切なフォルダーに格納します。 Outlook が、すべての重要なデータを含む可能性があると見なされる場合、Outlook は競合するコピーを [同期の問題] フォルダーの [競合] フォルダーに保存します。 
  
> [!NOTE]
> ナビゲーション ウィンドウで [フォルダー一覧] をクリックするまで、同期の問題とそのサブフォルダーは非表示になります。 
  
このような場合、ユーザーは Conflicts フォルダーに移動して、競合しているアイテムと、競合フォルダー内のコピーを使用して、保持することを決定したコピーを置き換えるかどうかを確認Outlook選択できます。
  
## <a name="conflict-resolution-for-custom-item-types"></a>カスタムアイテムの種類に対する競合の解決

### <a name="item-types-and-message-classes"></a>アイテムの種類とメッセージ クラス
  
メッセージ クラスにOutlook内のすべてのアイテムが関連付けられる。 たとえば、既定では、メール アイテムはメッセージ クラス **IPM に関連付けされます。注**. メッセージ クラスは、主に、アイテムをフォームに表示するために使用するフォームを識別Outlook。 Outlookに組み込むアイテムの種類にマップされるメッセージ クラスの一覧がサポートOutlook。 メッセージ クラスの詳細については、「[Item Types and Message Classes](https://msdn.microsoft.com/library/15b709cc-7486-b6c7-88a3-4a4d8e0ab292%28Office.15%29.aspx)」をご覧ください。 
  
ユーザーは、カスタム アイテムの種類を作成し、カスタム メッセージ クラスをカスタム アイテムの種類に割り当て、カスタム Outlookフォームを使用してカスタム アイテムの種類を表示できます。 たとえば、ビジネス連絡先のカスタムOutlookフォームを表示する必要がある場合があります。 これを行うには、カスタム メッセージ クラス **IPM を作成できます。Contact.Business 、** このメッセージ クラスのカスタム フォームを作成し、このメッセージ クラスでビジネス連絡先を割り当てる。 
  
### <a name="registering-a-conflict-resolution-scheme-for-custom-item-types"></a>カスタム アイテムの種類に対する競合解決スキームの登録
  
カスタム メッセージ クラスとカスタム フォーム以外のカスタム アイテムの種類を作成する場合は、Outlook でこのアイテムの種類のアイテムのコピー間の競合を処理する方法も考慮する必要があります。 既定では、Outlook では、すべてのアイテムに共通の解決スキームが採用され、アイテムの種類に固有のプロパティは考慮されません。また、ユーザーが決定を下す際に競合するコピーが表示されます。 これは、カスタム アイテムの種類がカスタム フォームでユーザー設定フィールドを定義し、カスタム プロパティとカスタム コードを持つ可能性があるためです。 アイテム固有のOutlookを検討し、最小限のユーザー介入で競合を解決しようとする場合は、レジストリの設定を使用してWindowsする必要があります。 これは、次の 2 つの方法のいずれかを使用して実現できます。 
  
- レジストリ キー ConflictMsgCls を設定するローカル コンピューターにグループ ポリシー設定を適用します。 次の例では、2010 年のバージョン "14.0" をOutlookします。 
  
   `[HKCU]\Software\Policies\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
- ユーザー レジストリ キー ConflictMsgCls を直接変更します。 次の例では、2010 年のバージョン "14.0" をOutlookします。 
  
   `[HKCU]\Software\Microsoft\Office\14.0\Outlook\Options\ConflictMsgCls`
    
グループ ポリシーによる競合解決の設定は、ユーザー レジストリ キーを直接変更するよりも優先されます。 レジストリ内のキーの場所は、レジストリのバージョンOutlook。 このキーの下に、カスタム メッセージ クラスの名前を値として指定します。 選択した解決方法に応じて、値の種類を **DWORD、** 値のデータを次の表に示す値の 1 つとして指定します。 
  
|データ  | 説明  |
|:-----|:-----|
|0  <br/> |2002 以前のバージョンで使用される、ユーザーの決定が必要Outlook一般的なアイテム解決。  <br/> |
|1  <br/> |2003 以降、ユーザーの介入を最小限に抑える一般的OutlookアイテムOutlookです。  <br/> |
|2  <br/> |メール アイテムに固有の解決。  <br/> |
|3  <br/> |会議アイテムに固有の解決。  <br/> |
|4  <br/> |予定アイテムに固有の解決。  <br/> |
|5  <br/> |連絡先アイテムに固有の解決策。  <br/> |
|6  <br/> |タスク アイテムに固有の解決。  <br/> |
|7  <br/> |付箋アイテムに固有の解像度。  <br/> |
|8  <br/> |ジャーナル アイテムに固有の解決。  <br/> |
   
アイテム固有の解決スキーム (キー データ 2 ~ 8) のいずれかを指定すると、Outlook はユーザーの介入なしにアイテム固有のフィールド (たとえば、予定アイテムの開始フィールドと終了フィールド) の競合を自動的に解決します。 Outlook が解決によって重要なデータが失われる可能性があると考える場合、Outlook は Conflicts フォルダー内の競合するコピーを保持し、ユーザーは Conflicts フォルダーに移動してこれらのアイテムを手動で再解決し、自動解決を上書きできます。 
  
カスタム メッセージ クラス IPM の連絡先アイテム固有の解決スキームを指定する場合は、上記の同じビジネス連絡先の例を **使用します。Contact.Business** では **、DWORD** 値としてデータとして追加し、  `[HKCU]\Software\Microsoft\Office\15.0\Outlook\Options\ConflictMsgCls` データとして 5 を指定できます。 
  
> [!NOTE]
> Outlookは、予定メッセージ クラス IPM に基づくカスタム メッセージ クラスの予定アイテムに固有の解決スキームを常に **使用します。予定** **(IPM など)。Appointment.Personal**)。 
  
## <a name="see-also"></a>関連項目

- [Outlook アイテム オブジェクト](https://msdn.microsoft.com/library/6ea4babf-facf-4018-ef5a-4a484e55153a%28Office.15%29.aspx)

