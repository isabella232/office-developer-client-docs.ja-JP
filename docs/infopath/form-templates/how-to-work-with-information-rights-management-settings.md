---
title: 使用可能な情報権利管理の設定
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- information rights management [infopath 2007],InfoPath 2007, Information Rights Management,IRM [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4ad91898-b23e-4410-8839-a65259e53d37
description: Microsoft InfoPath には、2 種類の Information Rights Management (IRM) 設定があります。1 つは InfoPath フォーム テンプレートへのアクセスを保護する設定、もう 1 つは入力されたフォームに含まれるフォーム データへのアクセスとその操作を制御する設定です。
ms.openlocfilehash: 4e6fdac6a0b2b5cd6a29de948cc9dbbd01a407d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799152"
---
# <a name="work-with-information-rights-management-settings"></a>使用可能な情報権利管理の設定

Microsoft InfoPath には、2 種類の Information Rights Management (IRM) 設定があります。1 つは InfoPath フォーム テンプレートへのアクセスを保護する設定、もう 1 つは入力されたフォームに含まれるフォーム データへのアクセスとその操作を制御する設定です。
  
> [!NOTE]
> [!メモ] アクセス許可の制限は、InfoPath エディターと互換性のあるフォーム テンプレートのみで利用できます。ブラウザー互換のフォーム テンプレートでは、IRM はサポートされません。 
  
## <a name="adding-the-manage-credentials-command-to-the-quick-access-toolbar"></a>クイック アクセス ツール バーへの [資格情報の管理] コマンドの追加

フォーム テンプレートのデザインが既定で利用できない場合に、以前は [ **資格情報の管理**] コマンドを使用して IRM 設定を操作していました。このコマンドを [ **クイック アクセス ツール バー**] に追加するには、次の手順に従います。
  
### <a name="add-the-manage-credentials-command-to-the-quick-access-toolbar"></a>クイック アクセス ツール バーに [資格情報の管理] コマンドを追加する

1.  [ **クイック アクセス ツール バー**] の右端の矢印をクリックして [ **クイック アクセス ツール バーのユーザー設定**] メニューを表示し、[ **その他のコマンド**] をクリックします。
    
2. [ **コマンドの選択**] の一覧から、[ **すべてのコマンド**] を選択します。
    
3. [ **資格情報の管理**] が表示されるまでスクロールして [ **追加**] をクリックします。
    
4. [ **OK**] をクリックします。
    
InfoPath の [ **資格情報の管理**] コマンドおよび [ **アクセス許可**] ダイアログ ボックスの使用方法の詳細については、InfoPath ヘルプで「アクセス制限のあるフォーム テンプレートを作成する」を参照してください。 
  
## <a name="the-irm-object-model"></a>IRM オブジェクト モデル

[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) クラスを使用して [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) およびフォームに適用できる IRM アクセス許可設定にアクセスします。フォーム テンプレートに関連付けられた **Permission** オブジェクトにアクセスするには、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) クラスの [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを使用します。返される **Permission** オブジェクトにより、フォーム テンプレートおよびそのテンプレートによって作成される各フォーム インスタンスに関連付けられた [UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) オブジェクトのコレクションへのアクセスが可能になります。 
  
**Permission** オブジェクトおよびそのプロパティとメソッドは、アクティブなフォーム テンプレートでアクセス許可が制限されているかどうかにかかわらず利用できます。フォームのアクセス許可が制限されているかどうかを判断するには、 [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) プロパティを使用します。 
  
フォームのアクセス許可は、Permission クラスのプロパティとメソッドを使用して、次のいずれかの方法で有効になっています。
  
**Enabled** プロパティを **true** に設定している。
  
[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) プロパティを設定している。 
  
[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) プロパティを設定している。 
  
[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) プロパティを **true** または **false** に設定している。
  
[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) メソッドを呼び出している。 
  
> [!NOTE]
> [!メモ] Windows Rights Management クライアントがユーザーのコンピューターにインストールされていない場合は、 **Permission** クラスを使用すると、例外が発生します。 
  
フォームで個別のユーザーの IRM 設定をプログラムによって操作するには、 **UserPermissionCollection** クラスおよび **UserPermission** クラスを使用します。 
  
**UserPermission** オブジェクトは、現在のフォームでのアクセス許可のセットを 1 人のユーザーおよびオプションの有効期限日に関連付けます。現在のフォームにアクセス許可のセットを追加し、ユーザーに付与するには、 [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) クラスの **Add** メソッドを使用します。ユーザーおよびユーザーのアクセス許可を削除するには、 [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) クラスの **Remove** メソッドを使用します。印刷や有効期限日など、ユーザー インターフェイスを通じて付与される一部のアクセス許可はすべてのユーザーに適用されますが、 **UserPermission** クラスおよび **UserPermissionCollection** クラスを使用すると、ユーザーおよびその有効期限日ごとにアクセス許可を割り当てることができます。このオブジェクト モデルにより、開発者はフォームのアクセス許可設定を列挙し、フォームのユーザーが [ **フォームのアクセス許可**] 作業ウィンドウまたは [ **アクセス許可**] ダイアログ ボックスを使用しなくても、フォームにアクセス許可を追加できるようにします。 
  
> [!NOTE]
> [!メモ] フォームがプレビュー モードの場合、アクセス許可を適用することはできません。このため、 **Permission** クラスのすべてのプロパティは、フォームのプレビュー時に読み取り専用になります。プレビュー モードでは、 **Enabled** プロパティは常に **false** を返します。コードでこの設定を変更しようとすると、 **System.Runtime.InteropServices.COMException** が発生し、"プロパティ/メソッドは、プレビュー モードで利用できません"というエラーが返されます。同様に、 **UserPermission** クラスおよび **UserPermissionCollection** クラスに関連付けられたメソッドも、プレビュー モードで使用するとこのエラー メッセージが返されます。 
  
### <a name="overview-of-the-permission-class"></a>Permission クラスの概要

**UserPermissionCollection** クラスには次のプロパティと 1 つのメソッドがあります。 
  
|**名前**|**説明**|
|:-----|:-----|
|[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) メソッド  <br/> |ポリシー テンプレート ファイルを使ってフォームにポリシーを適用します。  <br/> |
|[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) プロパティ  <br/> |取得または現在のフォームの作成者を電子メール アドレスとして設定します。  <br/> |
|[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) プロパティ  <br/> |**Permission** オブジェクトによって表されるアクセス許可設定が、現在のフォームで有効になっているかどうかを取得または設定します。  <br/> |
|[PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) プロパティ  <br/> |現在のフォームにアクセス許可ポリシーが適用されているかどうかを取得または設定します。  <br/> |
|[PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) プロパティ  <br/> |現在のフォームに適用されたポリシーの説明を取得します。  <br/> |
|[PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) プロパティ  <br/> |現在のフォームに適用されたポリシーの名前を取得します。  <br/> |
|[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) プロパティ  <br/> |取得または現在のフォームで追加のアクセス許可を必要としているユーザーに連絡するには、ファイル、URL、または電子メール アドレスを設定します。  <br/> |
|[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) プロパティ  <br/> |現在のフォームを表示するユーザーのライセンスをキャッシュし、ユーザーがアクセス権管理サーバーに接続できないときに、オフラインの表示を許可するかどうかを取得または設定します。  <br/> |
|[UserPermissions](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) プロパティ  <br/> |現在のフォームの **UserPermissionCollection** オブジェクトを取得します。  <br/> |
   
### <a name="overview-of-the-userpermissioncollection-class"></a>UserPermissionCollection クラスの概要

**UserPermissionCollection** クラスには次のプロパティとメソッドがあります。 
  
|**名前**|**説明**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) メソッド (+3 オーバーロード)  <br/> |現在のフォームに新しいユーザーを追加し、オプションでアクセス許可および有効期限日を指定します。  <br/> |
|[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) メソッド  <br/> |指定した **UserId** を持つ **UserPermission** オブジェクトをコレクションから削除します。  <br/> |
|[RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) メソッド  <br/> |すべての **UserPermission** オブジェクトをコレクションから削除します。  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx) プロパティ  <br/> |コレクションに含まれている **UserPermission** オブジェクトの数を取得します。  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) プロパティ (+1 オーバーロード)  <br/> |**UserPermission** オブジェクトを取得します。  <br/> |
   
### <a name="overview-of-the-userpermission-class"></a>UserPermission クラスの概要

**UserPermission** クラスには次のプロパティと 1 つのメソッドがあります。 
  
|**名前**|**説明**|
|:-----|:-----|
|[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx) メソッド  <br/> |現在の **UserPermission** オブジェクトをフォームのアクセス許可から削除します。  <br/> |
|[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) プロパティ  <br/> |**UserPermission** クラスのインスタンスに関連するユーザーに割り当てられた、現在のフォームでのアクセス許可のオプションの有効期限日を取得または設定します。  <br/> |
|[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) プロパティ  <br/> |**UserPermission** クラスのインスタンスに関連するユーザーに割り当てられた、現在のフォームのアクセス許可を表す値を取得または設定します。  <br/> |
|[UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) プロパティ  <br/> |現在のフォームに対するアクセス許可は、指定した**UserPermission**オブジェクトによって決定されますユーザーの電子メール アドレスを取得します。  <br/> |
   
### <a name="the-permissiontype-enumeration"></a>PermissionType 列挙

ユーザーのアクセス許可は、[PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) 列挙値を使用して設定または読み取られます。 
  
|**名前**|**説明**|
|:-----|:-----|
|**PermissionType.Change** <br/> |ユーザーによるフォームの表示、編集、コピー、および保存を許可しますが、印刷は許可しません。 **Read**、 **Edit**、 **Save**、および **Extract** のアクセス許可の組み合わせと同等です。  <br/> |
|**PermissionType.Edit** <br/> |ユーザーによるフォームの編集を許可します。  <br/> |
|**PermissionType.Extract** <br/> |**Read** アクセス許可を持つユーザーがフォームの内容をコピーすることを許可します。  <br/> |
|**PermissionType.FullControl** <br/> |ユーザーがフォームの他のユーザーのアクセス許可を追加、変更、および削除することを許可します。  <br/> |
|**PermissionType.ObjectModel** <br/> |ユーザーがオブジェクト モデルを使用してプログラムによってフォーム ドキュメントにアクセスすることを許可します。 **ObjectModel** アクセス許可のないユーザーは、オブジェクト モデルを使用してユーザー自身のアクセス許可を決定することができません。  <br/> |
|**PermissionType.Print** <br/> |ユーザーによるフォームの印刷を許可します。  <br/> |
|**PermissionType.Read** <br/> |ユーザーによるフォームの読み取り (表示) を許可します。( **Read** および **View** アクセス許可はこれと同等。)  <br/> |
|**PermissionType.Save** <br/> |ユーザーによるフォームの保存を許可します。  <br/> |
|**PermissionType.View** <br/> |ユーザーによるフォームの表示 (読み取り) を許可します。( **Read** および **View** アクセス許可はこれと同等。)  <br/> |
   
### <a name="example"></a>例

次の例では、[ **ボタン**] コントロールをクリックすると、現在のフォームの **UserPermissionsCollection** が取得され、Change アクセス レベルにユーザーが追加されて割り当てられ、有効期限日が現在の日付から 2 日後に設定されます。 
  
```cs
public void CTRL1_Clicked(object sender, ClickedEventArgs e)
{
   string strExpirationDate = DateTime.Today.AddDays(2).ToString();
   DateTime dtExpirationDate = DateTime.Parse(strExpirationDate);
   this.Permission.UserPermissions.Add("someone@example.com", 
      PermissionType.Change, dtExpirationDate);
}
```

```vb
Public Sub CTRL1_Clicked(ByVal sender As Object, _
   ByVal e As ClickedEventArgs)
   Dim strExpirationDate As String = _
      DateTime.Today.AddDays(2).ToString()
   dtExpirationDate As DateTime = DateTime.Parse(strExpirationDate)
   Me.Permission.UserPermissions.Add("someone@example.com", _
      PermissionType.Change, dtExpirationDate)
End Sub
```


