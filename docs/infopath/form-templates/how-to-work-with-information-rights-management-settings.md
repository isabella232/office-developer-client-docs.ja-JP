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
# <a name="work-with-information-rights-management-settings"></a><span data-ttu-id="494ec-104">使用可能な情報権利管理の設定</span><span class="sxs-lookup"><span data-stu-id="494ec-104">Work with Information Rights Management Settings</span></span>

<span data-ttu-id="494ec-105">Microsoft InfoPath には、2 種類の Information Rights Management (IRM) 設定があります。1 つは InfoPath フォーム テンプレートへのアクセスを保護する設定、もう 1 つは入力されたフォームに含まれるフォーム データへのアクセスとその操作を制御する設定です。</span><span class="sxs-lookup"><span data-stu-id="494ec-105">There are two types of Information Rights Management (IRM) settings available in Microsoft InfoPath: one for protecting access to InfoPath form templates, and one for controlling access to and actions on form data contained in completed forms.</span></span>
  
> [!NOTE]
> <span data-ttu-id="494ec-p101">[!メモ] アクセス許可の制限は、InfoPath エディターと互換性のあるフォーム テンプレートのみで利用できます。ブラウザー互換のフォーム テンプレートでは、IRM はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="494ec-p101">Restricting permission is only available to form templates compatible with the InfoPath editor. Browser-compatible form templates do not support IRM.</span></span> 
  
## <a name="adding-the-manage-credentials-command-to-the-quick-access-toolbar"></a><span data-ttu-id="494ec-108">クイック アクセス ツール バーへの [資格情報の管理] コマンドの追加</span><span class="sxs-lookup"><span data-stu-id="494ec-108">Adding the Manage Credentials Command to the Quick Access Toolbar</span></span>

<span data-ttu-id="494ec-p102">フォーム テンプレートのデザインが既定で利用できない場合に、以前は [ **資格情報の管理**] コマンドを使用して IRM 設定を操作していました。このコマンドを [ **クイック アクセス ツール バー**] に追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="494ec-p102">The **Manage Credentials** command used to work with IRM settings when designing a form template is not available by default. Use the following steps to add it to the **Quick Access Toolbar**.</span></span>
  
### <a name="add-the-manage-credentials-command-to-the-quick-access-toolbar"></a><span data-ttu-id="494ec-111">クイック アクセス ツール バーに [資格情報の管理] コマンドを追加する</span><span class="sxs-lookup"><span data-stu-id="494ec-111">Add the Manage Credentials Command to the Quick Access Toolbar</span></span>

1.  <span data-ttu-id="494ec-112">[ **クイック アクセス ツール バー**] の右端の矢印をクリックして [ **クイック アクセス ツール バーのユーザー設定**] メニューを表示し、[ **その他のコマンド**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="494ec-112">Click the arrow on the right end of the **Quick Access Toolbar** to pull down the **Customize Quick Access Toolbar** menu, and then click **More Commands**.</span></span>
    
2. <span data-ttu-id="494ec-113">[ **コマンドの選択**] の一覧から、[ **すべてのコマンド**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="494ec-113">In the **Choose commands from** list, select **All Commands**.</span></span>
    
3. <span data-ttu-id="494ec-114">[ **資格情報の管理**] が表示されるまでスクロールして [ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="494ec-114">Scroll down the list to **Manage Credentials**, and then click **Add**.</span></span>
    
4. <span data-ttu-id="494ec-115">[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="494ec-115">Click **OK**.</span></span>
    
<span data-ttu-id="494ec-116">InfoPath の [ **資格情報の管理**] コマンドおよび [ **アクセス許可**] ダイアログ ボックスの使用方法の詳細については、InfoPath ヘルプで「アクセス制限のあるフォーム テンプレートを作成する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="494ec-116">For more information about using **Manage Credentials** command and the **Permission** dialog box in InfoPath, see the "Create a Form Template with Restricted Permission" topic in InfoPath help.</span></span> 
  
## <a name="the-irm-object-model"></a><span data-ttu-id="494ec-117">IRM オブジェクト モデル</span><span class="sxs-lookup"><span data-stu-id="494ec-117">The IRM Object Model</span></span>

<span data-ttu-id="494ec-p103">[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) クラスを使用して [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) およびフォームに適用できる IRM アクセス許可設定にアクセスします。フォーム テンプレートに関連付けられた **Permission** オブジェクトにアクセスするには、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) クラスの [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを使用します。返される **Permission** オブジェクトにより、フォーム テンプレートおよびそのテンプレートによって作成される各フォーム インスタンスに関連付けられた [UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) オブジェクトのコレクションへのアクセスが可能になります。</span><span class="sxs-lookup"><span data-stu-id="494ec-p103">Use the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) class to access the [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) and IRM permission settings that can be applied to a form. To access the **Permission** object associated with a form template, use the [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class. The returned **Permission** object provides access to the collection of [UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) objects associated with the form template and each form instance created with that template.</span></span> 
  
<span data-ttu-id="494ec-p104">**Permission** オブジェクトおよびそのプロパティとメソッドは、アクティブなフォーム テンプレートでアクセス許可が制限されているかどうかにかかわらず利用できます。フォームのアクセス許可が制限されているかどうかを判断するには、 [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="494ec-p104">The **Permission** object and its properties and methods are available whether permissions are restricted on the active form template or not. Use the [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) property to determine whether a form has restricted permissions.</span></span> 
  
<span data-ttu-id="494ec-123">フォームのアクセス許可は、Permission クラスのプロパティとメソッドを使用して、次のいずれかの方法で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="494ec-123">Permissions on a form are enabled in one of the following ways by using properties and methods of the Permission class:</span></span>
  
<span data-ttu-id="494ec-124">**Enabled** プロパティを **true** に設定している。</span><span class="sxs-lookup"><span data-stu-id="494ec-124">The **Enabled** property is set to **true**.</span></span>
  
<span data-ttu-id="494ec-125">[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) プロパティを設定している。</span><span class="sxs-lookup"><span data-stu-id="494ec-125">The [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) property is set.</span></span> 
  
<span data-ttu-id="494ec-126">[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) プロパティを設定している。</span><span class="sxs-lookup"><span data-stu-id="494ec-126">The [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) property is set.</span></span> 
  
<span data-ttu-id="494ec-127">[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) プロパティを **true** または **false** に設定している。</span><span class="sxs-lookup"><span data-stu-id="494ec-127">The [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) property is set to **true** or **false**.</span></span>
  
<span data-ttu-id="494ec-128">[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) メソッドを呼び出している。</span><span class="sxs-lookup"><span data-stu-id="494ec-128">The [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) method is called.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="494ec-129">[!メモ] Windows Rights Management クライアントがユーザーのコンピューターにインストールされていない場合は、 **Permission** クラスを使用すると、例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="494ec-129">If the Windows Rights Management client is not installed on a user's computer, using the **Permission** class raises an exception.</span></span> 
  
<span data-ttu-id="494ec-130">フォームで個別のユーザーの IRM 設定をプログラムによって操作するには、 **UserPermissionCollection** クラスおよび **UserPermission** クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="494ec-130">To work programmatically with IRM settings of individual users in forms, use the **UserPermissionCollection** and **UserPermission** classes.</span></span> 
  
<span data-ttu-id="494ec-p105">**UserPermission** オブジェクトは、現在のフォームでのアクセス許可のセットを 1 人のユーザーおよびオプションの有効期限日に関連付けます。現在のフォームにアクセス許可のセットを追加し、ユーザーに付与するには、 [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) クラスの **Add** メソッドを使用します。ユーザーおよびユーザーのアクセス許可を削除するには、 [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) クラスの **Remove** メソッドを使用します。印刷や有効期限日など、ユーザー インターフェイスを通じて付与される一部のアクセス許可はすべてのユーザーに適用されますが、 **UserPermission** クラスおよび **UserPermissionCollection** クラスを使用すると、ユーザーおよびその有効期限日ごとにアクセス許可を割り当てることができます。このオブジェクト モデルにより、開発者はフォームのアクセス許可設定を列挙し、フォームのユーザーが [ **フォームのアクセス許可**] 作業ウィンドウまたは [ **アクセス許可**] ダイアログ ボックスを使用しなくても、フォームにアクセス許可を追加できるようにします。</span><span class="sxs-lookup"><span data-stu-id="494ec-p105">A **UserPermission** object associates a set of permissions for the current form with a single user and an optional expiration date. Use the [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) method of the **UserPermissionCollection** class to add and grant a user a set of permissions on the current form. Use the [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) method of the **UserPermissionCollection** class to remove a user and the user's permissions. While some permissions granted through the user interface apply to all users, such as printing and expiration date, you can use the **UserPermission** and **UserPermissionCollection** classes to assign them on a per-user basis with per-user expiration dates. The object model allows developers to enumerate permission settings in a form and to provide functionality that allows form users to add permissions to the form without having to use the **Form Permission** task pane or the **Permission** dialog box.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="494ec-p106">[!メモ] フォームがプレビュー モードの場合、アクセス許可を適用することはできません。このため、 **Permission** クラスのすべてのプロパティは、フォームのプレビュー時に読み取り専用になります。プレビュー モードでは、 **Enabled** プロパティは常に **false** を返します。コードでこの設定を変更しようとすると、 **System.Runtime.InteropServices.COMException** が発生し、"プロパティ/メソッドは、プレビュー モードで利用できません"というエラーが返されます。同様に、 **UserPermission** クラスおよび **UserPermissionCollection** クラスに関連付けられたメソッドも、プレビュー モードで使用するとこのエラー メッセージが返されます。</span><span class="sxs-lookup"><span data-stu-id="494ec-p106">Permissions cannot be applied when a form is in preview mode. For this reason, all of the properties of the **Permission** class are read-only when a form is being previewed. In preview mode, the **Enabled** property will always return **false**, and if code attempts to change this setting, a **System.Runtime.InteropServices.COMException** is raised and the error "The property/method is not available in preview mode" is returned. Similarly, the methods associated with the **UserPermission** and **UserPermissionCollection** classes will also return this error message when used in preview mode.</span></span> 
  
### <a name="overview-of-the-permission-class"></a><span data-ttu-id="494ec-140">Permission クラスの概要</span><span class="sxs-lookup"><span data-stu-id="494ec-140">Overview of the Permission Class</span></span>

<span data-ttu-id="494ec-141">**UserPermissionCollection** クラスには次のプロパティと 1 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="494ec-141">The **UserPermissionCollection** class provides the following properties and one method.</span></span> 
  
|<span data-ttu-id="494ec-142">**名前**</span><span class="sxs-lookup"><span data-stu-id="494ec-142">**Name**</span></span>|<span data-ttu-id="494ec-143">**説明**</span><span class="sxs-lookup"><span data-stu-id="494ec-143">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="494ec-144">[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="494ec-144">[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) method</span></span>  <br/> |<span data-ttu-id="494ec-145">ポリシー テンプレート ファイルを使ってフォームにポリシーを適用します。</span><span class="sxs-lookup"><span data-stu-id="494ec-145">Applies a policy to the form using a policy template file.</span></span>  <br/> |
|<span data-ttu-id="494ec-146">[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-146">[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-147">取得または現在のフォームの作成者を電子メール アドレスとして設定します。</span><span class="sxs-lookup"><span data-stu-id="494ec-147">Gets or sets the author of the current form as an email address.</span></span>  <br/> |
|<span data-ttu-id="494ec-148">[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-148">[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-149">**Permission** オブジェクトによって表されるアクセス許可設定が、現在のフォームで有効になっているかどうかを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="494ec-149">Gets or sets whether the permission settings represented by the **Permission** object are enabled for the current form.</span></span>  <br/> |
|<span data-ttu-id="494ec-150">[PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-150">[PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-151">現在のフォームにアクセス許可ポリシーが適用されているかどうかを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="494ec-151">Gets or sets whether a permission policy has been applied to the current form.</span></span>  <br/> |
|<span data-ttu-id="494ec-152">[PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-152">[PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-153">現在のフォームに適用されたポリシーの説明を取得します。</span><span class="sxs-lookup"><span data-stu-id="494ec-153">Gets a description of the policy that was applied to the current form.</span></span>  <br/> |
|<span data-ttu-id="494ec-154">[PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-154">[PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-155">現在のフォームに適用されたポリシーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="494ec-155">Gets the name of the policy that was applied to the current form.</span></span>  <br/> |
|<span data-ttu-id="494ec-156">[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-156">[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-157">取得または現在のフォームで追加のアクセス許可を必要としているユーザーに連絡するには、ファイル、URL、または電子メール アドレスを設定します。</span><span class="sxs-lookup"><span data-stu-id="494ec-157">Gets or sets the file, URL, or email address to contact for users who need additional permissions on the current form.</span></span>  <br/> |
|<span data-ttu-id="494ec-158">[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-158">[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-159">現在のフォームを表示するユーザーのライセンスをキャッシュし、ユーザーがアクセス権管理サーバーに接続できないときに、オフラインの表示を許可するかどうかを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="494ec-159">Gets or sets whether the user's license to view the current form should be cached to allow offline viewing when the user cannot connect to a rights management server.</span></span>  <br/> |
|<span data-ttu-id="494ec-160">[UserPermissions](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-160">[UserPermissions](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-161">現在のフォームの **UserPermissionCollection** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="494ec-161">Gets a **UserPermissionCollection** object for the current form.</span></span>  <br/> |
   
### <a name="overview-of-the-userpermissioncollection-class"></a><span data-ttu-id="494ec-162">UserPermissionCollection クラスの概要</span><span class="sxs-lookup"><span data-stu-id="494ec-162">Overview of the UserPermissionCollection Class</span></span>

<span data-ttu-id="494ec-163">**UserPermissionCollection** クラスには次のプロパティとメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="494ec-163">The **UserPermissionCollection** class provides the following properties and methods.</span></span> 
  
|<span data-ttu-id="494ec-164">**名前**</span><span class="sxs-lookup"><span data-stu-id="494ec-164">**Name**</span></span>|<span data-ttu-id="494ec-165">**説明**</span><span class="sxs-lookup"><span data-stu-id="494ec-165">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="494ec-166">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) メソッド (+3 オーバーロード)</span><span class="sxs-lookup"><span data-stu-id="494ec-166">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) method (+3 overloads)</span></span>  <br/> |<span data-ttu-id="494ec-167">現在のフォームに新しいユーザーを追加し、オプションでアクセス許可および有効期限日を指定します。</span><span class="sxs-lookup"><span data-stu-id="494ec-167">Adds a new user to the current form, optionally specifying permissions and an expiration date.</span></span>  <br/> |
|<span data-ttu-id="494ec-168">[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="494ec-168">[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) method</span></span>  <br/> |<span data-ttu-id="494ec-169">指定した **UserId** を持つ **UserPermission** オブジェクトをコレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="494ec-169">Removes the **UserPermission** object with the specified **UserId** from the collection.</span></span>  <br/> |
|<span data-ttu-id="494ec-170">[RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="494ec-170">[RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) method</span></span>  <br/> |<span data-ttu-id="494ec-171">すべての **UserPermission** オブジェクトをコレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="494ec-171">Removes all **UserPermission** objects from the collection.</span></span>  <br/> |
|<span data-ttu-id="494ec-172">[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-172">[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-173">コレクションに含まれている **UserPermission** オブジェクトの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="494ec-173">Gets the number of **UserPermission** objects in the collection.</span></span>  <br/> |
|<span data-ttu-id="494ec-174">[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) プロパティ (+1 オーバーロード)</span><span class="sxs-lookup"><span data-stu-id="494ec-174">[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) property (+1 overload)</span></span>  <br/> |<span data-ttu-id="494ec-175">**UserPermission** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="494ec-175">Gets a **UserPermission** object.</span></span>  <br/> |
   
### <a name="overview-of-the-userpermission-class"></a><span data-ttu-id="494ec-176">UserPermission クラスの概要</span><span class="sxs-lookup"><span data-stu-id="494ec-176">Overview of the UserPermission Class</span></span>

<span data-ttu-id="494ec-177">**UserPermission** クラスには次のプロパティと 1 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="494ec-177">The **UserPermission** class provides the following properties and one method.</span></span> 
  
|<span data-ttu-id="494ec-178">**名前**</span><span class="sxs-lookup"><span data-stu-id="494ec-178">**Name**</span></span>|<span data-ttu-id="494ec-179">**説明**</span><span class="sxs-lookup"><span data-stu-id="494ec-179">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="494ec-180">[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="494ec-180">[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx) method</span></span>  <br/> |<span data-ttu-id="494ec-181">現在の **UserPermission** オブジェクトをフォームのアクセス許可から削除します。</span><span class="sxs-lookup"><span data-stu-id="494ec-181">Removes the current **UserPermission** object from the form's permissions.</span></span>  <br/> |
|<span data-ttu-id="494ec-182">[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-182">[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-183">**UserPermission** クラスのインスタンスに関連するユーザーに割り当てられた、現在のフォームでのアクセス許可のオプションの有効期限日を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="494ec-183">Gets or sets the optional expiration date for the permissions on the current form assigned to the user associated with an instance of the **UserPermission** class.</span></span>  <br/> |
|<span data-ttu-id="494ec-184">[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-184">[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-185">**UserPermission** クラスのインスタンスに関連するユーザーに割り当てられた、現在のフォームのアクセス許可を表す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="494ec-185">Gets or sets a value representing the permissions on the current form assigned to the user associated with an instance of the **UserPermission** class.</span></span>  <br/> |
|<span data-ttu-id="494ec-186">[UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="494ec-186">[UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) property</span></span>  <br/> |<span data-ttu-id="494ec-187">現在のフォームに対するアクセス許可は、指定した**UserPermission**オブジェクトによって決定されますユーザーの電子メール アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="494ec-187">Gets the email address of the user whose permissions on the current form are determined by the specified **UserPermission** object.</span></span>  <br/> |
   
### <a name="the-permissiontype-enumeration"></a><span data-ttu-id="494ec-188">PermissionType 列挙</span><span class="sxs-lookup"><span data-stu-id="494ec-188">The PermissionType Enumeration</span></span>

<span data-ttu-id="494ec-189">ユーザーのアクセス許可は、[PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) 列挙値を使用して設定または読み取られます。</span><span class="sxs-lookup"><span data-stu-id="494ec-189">A user's permissions are set or read using [PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) enumeration values.</span></span> 
  
|<span data-ttu-id="494ec-190">**名前**</span><span class="sxs-lookup"><span data-stu-id="494ec-190">**Name**</span></span>|<span data-ttu-id="494ec-191">**説明**</span><span class="sxs-lookup"><span data-stu-id="494ec-191">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="494ec-192">**PermissionType.Change**</span><span class="sxs-lookup"><span data-stu-id="494ec-192">**PermissionType.Change**</span></span> <br/> |<span data-ttu-id="494ec-p107">ユーザーによるフォームの表示、編集、コピー、および保存を許可しますが、印刷は許可しません。 **Read**、 **Edit**、 **Save**、および **Extract** のアクセス許可の組み合わせと同等です。  </span><span class="sxs-lookup"><span data-stu-id="494ec-p107">Allows users to view, edit, copy, and save, but not print a form. Equivalent to the **Read**, **Edit**, **Save**, and **Extract** permissions combined.  </span></span><br/> |
|<span data-ttu-id="494ec-195">**PermissionType.Edit**</span><span class="sxs-lookup"><span data-stu-id="494ec-195">**PermissionType.Edit**</span></span> <br/> |<span data-ttu-id="494ec-196">ユーザーによるフォームの編集を許可します。</span><span class="sxs-lookup"><span data-stu-id="494ec-196">Allows the user to edit the form.</span></span>  <br/> |
|<span data-ttu-id="494ec-197">**PermissionType.Extract**</span><span class="sxs-lookup"><span data-stu-id="494ec-197">**PermissionType.Extract**</span></span> <br/> |<span data-ttu-id="494ec-198">**Read** アクセス許可を持つユーザーがフォームの内容をコピーすることを許可します。</span><span class="sxs-lookup"><span data-stu-id="494ec-198">Allows a user with the **Read** permission to copy content in the form.</span></span>  <br/> |
|<span data-ttu-id="494ec-199">**PermissionType.FullControl**</span><span class="sxs-lookup"><span data-stu-id="494ec-199">**PermissionType.FullControl**</span></span> <br/> |<span data-ttu-id="494ec-200">ユーザーがフォームの他のユーザーのアクセス許可を追加、変更、および削除することを許可します。</span><span class="sxs-lookup"><span data-stu-id="494ec-200">Allows the user to add, change, and remove permissions for other users of a form.</span></span>  <br/> |
|<span data-ttu-id="494ec-201">**PermissionType.ObjectModel**</span><span class="sxs-lookup"><span data-stu-id="494ec-201">**PermissionType.ObjectModel**</span></span> <br/> |<span data-ttu-id="494ec-p108">ユーザーがオブジェクト モデルを使用してプログラムによってフォーム ドキュメントにアクセスすることを許可します。 **ObjectModel** アクセス許可のないユーザーは、オブジェクト モデルを使用してユーザー自身のアクセス許可を決定することができません。  </span><span class="sxs-lookup"><span data-stu-id="494ec-p108">Allows a user to access the form document programmatically through its object model. Users without the **ObjectModel** permission cannot use the object model to determine their own permissions.  </span></span><br/> |
|<span data-ttu-id="494ec-204">**PermissionType.Print**</span><span class="sxs-lookup"><span data-stu-id="494ec-204">**PermissionType.Print**</span></span> <br/> |<span data-ttu-id="494ec-205">ユーザーによるフォームの印刷を許可します。</span><span class="sxs-lookup"><span data-stu-id="494ec-205">Allows the user to print the form.</span></span>  <br/> |
|<span data-ttu-id="494ec-206">**PermissionType.Read**</span><span class="sxs-lookup"><span data-stu-id="494ec-206">**PermissionType.Read**</span></span> <br/> |<span data-ttu-id="494ec-p109">ユーザーによるフォームの読み取り (表示) を許可します。( **Read** および **View** アクセス許可はこれと同等。)  </span><span class="sxs-lookup"><span data-stu-id="494ec-p109">Allows the user to read (view) the form. (The **Read** and **View** permissions are equivalent.)  </span></span><br/> |
|<span data-ttu-id="494ec-209">**PermissionType.Save**</span><span class="sxs-lookup"><span data-stu-id="494ec-209">**PermissionType.Save**</span></span> <br/> |<span data-ttu-id="494ec-210">ユーザーによるフォームの保存を許可します。</span><span class="sxs-lookup"><span data-stu-id="494ec-210">Allows the user to save the form.</span></span>  <br/> |
|<span data-ttu-id="494ec-211">**PermissionType.View**</span><span class="sxs-lookup"><span data-stu-id="494ec-211">**PermissionType.View**</span></span> <br/> |<span data-ttu-id="494ec-p110">ユーザーによるフォームの表示 (読み取り) を許可します。( **Read** および **View** アクセス許可はこれと同等。)  </span><span class="sxs-lookup"><span data-stu-id="494ec-p110">Allows the user to view (read) the form. (The **Read** and **View** permissions are equivalent.)  </span></span><br/> |
   
### <a name="example"></a><span data-ttu-id="494ec-214">例</span><span class="sxs-lookup"><span data-stu-id="494ec-214">Example</span></span>

<span data-ttu-id="494ec-215">次の例では、[ **ボタン**] コントロールをクリックすると、現在のフォームの **UserPermissionsCollection** が取得され、Change アクセス レベルにユーザーが追加されて割り当てられ、有効期限日が現在の日付から 2 日後に設定されます。</span><span class="sxs-lookup"><span data-stu-id="494ec-215">In the following example, clicking the **Button** control gets the **UserPermissionsCollection** for the current form, adds and assigns a user to the Change access level, and sets an expiration date of two days from the current date.</span></span> 
  
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

