---



copyright:

  years: 2015, 2018
lastupdated: "2018-04-18"

---


{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} (bx) コマンド
{: #bluemix_cli}

バージョン: 0.6.7

{{site.data.keyword.Bluemix_notm}} コマンド・ライン・インターフェース (CLI) では、ユーザーが {{site.data.keyword.Bluemix_notm}} と対話できるように、名前空間別にグループ化したコマンドのセットが提供されています。

バージョン 0.5.0 以降、{{site.data.keyword.Bluemix_notm}} コマンド・ライン・クライアントは、Cloud Foundry コマンド・ライン・クライアントをインストール済み環境にバンドルしています。 独自の cf cli がインストールされている場合は、{{site.data.keyword.Bluemix_notm}} CLI コマンド `bx [command]` と、独自のインストール済み環境の Cloud Foundry CLI コマンド `cf [command]` の両方を同じコンテキストで使用しないでください。 cf cli を使用して {{site.data.keyword.Bluemix_notm}} CLI コンテキストで Cloud Foundry リソースを管理したい場合は、代わりに `bluemix cf [command]` を使用してください。  `bluemix cf api/login/logout/target` は使用できないので注意してください。代わりに、`bluemix api/login/logout/target` を使用してください。

名前、引数、オプション、前提条件、説明、および例を含め、{{site.data.keyword.Bluemix_notm}} CLI でサポートされている詳細なコマンドを以下にリストします。
{:shortdesc}

**注:** *前提条件*には、コマンドを使用する前に必要なアクションがリストされています。 前提条件となるアクションのないコマンドでは、**なし**とリストされています。 それ以外の場合、前提条件には以下のアクションのうちの 1 つ以上が含まれます。

<dl>
<dt>エンドポイント</dt>
<dd>このコマンドを使用する前に、<code>bluemix api</code> を介して API エンドポイントを設定する必要があります。</dd>
<dt>ログイン</dt>
<dd>このコマンドを使用する前に、<code>bluemix login</code> コマンドを使用してログインする必要があります。
フェデレーテッド ID でログインする場合は、「--sso」オプションを使用してワンタイム・パスコードで認証するか、「--apikey」を使用して API キーで認証します。 {{site.data.keyword.Bluemix_notm}} コンソールで**「管理」** &gt; **「セキュリティー」** &gt; **「プラットフォーム API キー」**に移動して、API キーを作成します。
</dd>
<dt>ターゲット</dt>
<dd>このコマンドを使用する前に、<code>bluemix target</code> コマンドを使用して組織およびスペースを設定する必要があります。</dd>
<dt>Docker</dt>
<dd>このコマンドを実行するためには、Docker CLI (docker) がインストールされている必要があります。</dd>
</dl>

**注:** 短形式の Bluemix コマンドを使用できます。例えば、`bx api` は `bluemix api` の短形式です。

以下の表の索引を使用して、使用頻度の高い bluemix コマンドを
参照してください。

## 汎用 Bluemix コマンド
{: #bx_commands_index}

<table summary="汎用 Bluemix コマンド。">
<caption>表 1. 汎用 bluemix コマンド</caption>
 <thead>
 <th colspan="5">汎用 Bluemix コマンド</th>
 </thead>
 <tbody>
 <tr>
 <td>[bluemix help](bx_cli.html#bluemix_help)</td>
 <td>[bluemix api](bx_cli.html#bluemix_api)</td>
 <td>[bluemix config](bx_cli.html#bluemix_config)</td>
 <td>[bluemix info
](bx_cli.html#bluemix_info)</td>
 <td>[bluemix cf](bx_cli.html#bluemix_cf)</td>
 </tr>
 <tr>
 <td>[bluemix login](bx_cli.html#bluemix_login) </td>
 <td>[bluemix logout](bx_cli.html#bluemix_logout) </td>
 <td>[bluemix regions](bx_cli.html#bluemix_regions)</td>
 <td>[bluemix target](bx_cli.html#bluemix_target)</td>
 <td>[bluemix update](bx_cli.html#bluemix_update)</td>
 </tr>
 </tbody>
 </table>

 ## {{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャー・サービスを管理および構成するためのコマンド (bluemix sl)
  {: #bx_commands_softlayer}

{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーを管理するためのコマンドは、{{site.data.keyword.Bluemix_notm}} CLI にマージされました。 {{site.data.keyword.Bluemix_notm}} CLI を使用した {{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャー・サービスの構成および管理について詳しくは、[{{site.data.keyword.Bluemix_notm}} CLI {{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャー (bluemix sl) コマンド](/docs/cli/reference/softlayer/index.md#softlayer_cli)を参照してください。

 ## アカウント、組織、および役割を管理するためのコマンド
 {: #bx_commands_account}

<table summary="アカウント、組織、スペース、および役割を管理するために使用できる bluemix コマンド。">
<caption>表 2. アカウント、組織、スペース、および役割を管理するためのコマンド</caption>
 <thead>
 <th colspan="5">アカウント、組織、スペース、および役割を管理するためのコマンド</th>
 </thead>
 <tbody>
 <tr>
 <td>[bluemix account orgs](bx_cli.html#bluemix_account_orgs)</td>
 <td>[bluemix account org](bx_cli.html#bluemix_account_org)</td>
 <td>[bluemix account org-create](bx_cli.html#bluemix_account_org_create)</td>
 <td>[bluemix account org-replicate](bx_cli.html#bluemix_account_org_replicate)</td>
 <td>[bluemix account org-rename](bx_cli.html#bluemix_account_org_rename)</td>
 </tr>
 <tr>
 <td>[bluemix account spaces](bx_cli.html#bluemix_account_spaces)</td>
 <td>[bluemix account space](bx_cli.html#bluemix_account_space)</td>
 <td>[bluemix account space-create](bx_cli.html#bluemix_account_space_create)</td>
 <td>[bluemix account space-rename](bx_cli.html#bluemix_account_space_rename)</td>
 <td>[bluemix account space-delete](bx_cli.html#bluemix_account_space_delete)</td>
 </tr>
 <tr>
 <td>[bluemix account org-users](bx_cli.html#bluemix_account_org_users)</td>
 <td>[bluemix account org-user-add](bx_cli.html#bluemix_account_org_user_add)</td>
 <td>[bluemix account org-user-remove](bx_cli.html#bluemix_account_org_user_remove)</td>
 <td>[bluemix account org-roles](bx_cli.html#bluemix_account_org_roles)</td>
 <td>[bluemix account org-role-set](bx_cli.html#bluemix_account_org_role_set)</td>
 </tr>
 <tr>
 <td>[bluemix account org-role-unset](bx_cli.html#bluemix_account_org_role_unset)</td>
 <td>[bluemix account space-users](bx_cli.html#bluemix_account_space_users)</td>
 <td>[bluemix account space-roles](bx_cli.html#bluemix_account_space_roles)</td>
 <td>[bluemix account space-role-set](bx_cli.html#bluemix_account_space_role_set)</td>
 <td>[bluemix account space-role-unset](bx_cli.html#bluemix_account_space_role_unset)</td>
</tr>
 <td>[bluemix account list](bx_cli.html#bluemix_account_list)</td>
 <td>[bluemix account org-account](bx_cli.html#bluemix_account_org_account)</td>
 <td>[bluemix account users](bx_cli.html#bluemix_account_users)</td>
 <td>[bluemix account users-delete](bx_cli.html#bluemix_account_users_delete)</td>
 <td>[bluemix account user-invite](bx_cli.html#bluemix_account_user_invite)</td>
 </tr>
 <tr>
  <td>[bluemix account user-reinvite](bx_cli.html#bluemix_account_user_reinvite)</td>
  <td>[bluemix iam access-groups](bx_cli.html#bluemix_iam_access-groups)</td>
  <td>[bluemix iam access-group](bx_cli.html#bluemix_iam_access-group)</td>
  <td>[bluemix iam access-group-create](bx_cli.html#bluemix_iam_access-group-create)</td>
  <td>[bluemix iam access-group-update](bx_cli.html#bluemix_iam_access-group-update)</td>
</tr>
<tr>
  <td>[bluemix iam access-group-delete](bx_cli.html#bluemix_iam_access-group-delete)</td>
  <td>[bluemix iam access-group-users](bx_cli.html#bluemix_iam_access-group-users)</td>
  <td>[bluemix iam access-group-user-add](bx_cli.html#bluemix_iam_access-group-user-add)</td>
  <td>[bluemix iam access-group-user-remove](bx_cli.html#bluemix_iam_access-group-user-remove)</td>
  <td>[bluemix iam access-group-user-purge](bx_cli.html#bluemix_iam_access-group-user-purge)</td>
</tr>
<tr>
  <td>[bluemix iam access-group-service-ids](bx_cli.html#bluemix_iam_access-group-service-ids)</td>
  <td>[bluemix iam access-group-service-id-add](bx_cli.html#bluemix_iam_access-group-service-id-add)</td>
  <td>[bluemix iam access-group-service-id-remove](bx_cli.html#bluemix_iam_access-group-service-id-remove)</td>
  <td>[bluemix iam access-group-service-id-purge](bx_cli.html#bluemix_iam_access-group-service-id-purge)</td>
  <td>[bluemix iam access-group-policies](bx_cli.html#bluemix_iam_access-group-policies)</td>
</tr>
<tr>
  <td>[bluemix iam access-group-policy](bx_cli.html#bluemix_iam_access-group-policy)</td>
  <td>[bluemix iam access-group-policy-create](bx_cli.html#bluemix_iam_access-group-policy-create)</td>
  <td>[bluemix iam access-group-policy-update](bx_cli.html#bluemix_iam_access-group-policy-update)</td>
  <td>[bluemix iam access-group-policy-delete](bx_cli.html#bluemix_iam_access-group-policy-delete)</td>
 </tr>
 </tbody>
 </table>


 ## リソース・グループとリソースを管理するためのコマンド
{: #bx_commands_resource}

<table summary="リソース・グループとリソースを管理するために使用できる bluemix コマンド。">
  <caption>表 3. リソース・グループとリソースを管理するためのコマンド</caption>
  <thead>
    <th colspan="5">リソース・グループとリソースを管理するためのコマンド</th>
  </thead>
  <tbody>
    <tr>
      <td>[bluemix resource groups](bx_cli.html#bluemix_resource_groups)</td>
      <td>[bluemix resource group](bx_cli.html#bluemix_resource_group)</td>
      <td>[bluemix resource group-update](bx_cli.html#bluemix_resource_group_update)</td>
      <td>[bluemix resource quotas](bx_cli.html#bluemix_resource_quotas)</td>
      <td>[bluemix resource quota](bx_cli.html#bluemix_resource_quota)</td>
    </tr>
    <tr>
      <td>[bluemix resource service-instances](bx_cli.html#bluemix_resource_service_instances)</td>
      <td>[bluemix resource service-instance](bx_cli.html#bluemix_resource_service_instance)</td>
      <td>[bluemix resource service-instance-create](bx_cli.html#bluemix_resource_service_instance_create)</td>
      <td>[bluemix resource service-instance-update](bx_cli.html#bluemix_resource_service_instance_update)</td>
      <td>[bluemix resource service-instance-delete](bx_cli.html#bluemix_resource_service_instance_delete)</td>
    </tr>
    <tr>
      <td>[bluemix resource service-bindings](bx_cli.html#bluemix_resource_service_bindings)</td>
      <td>[bluemix resource service-binding](bx_cli.html#bluemix_resource_service_binding)</td>
      <td>[bluemix resource service-binding-create](bx_cli.html#bluemix_resource_service_binding_create)</td>
      <td>[bluemix resource service-binding-delete](bx_cli.html#bluemix_resource_service_binding_delete)</td>
    </tr>
    <tr>
      <td>[bluemix resource service-keys](bx_cli.html#bluemix_resource_service_keys)</td>
      <td>[bluemix resource service-key](bx_cli.html#bluemix_resource_service_key)</td>
      <td>[bluemix resource service-key-create](bx_cli.html#bluemix_resource_service_key_create)</td>
      <td>[bluemix resource service-key-delete](bx_cli.html#bluemix_resource_service_key_delete)</td>
    </tr>
    <tr>
      <td>[bluemix resource service-aliases](bx_cli.html#bluemix_resource_service_aliases)</td>
      <td>[bluemix resource service-alias](bx_cli.html#bluemix_resource_service_alias)</td>
      <td>[bluemix resource service-alias-create](bx_cli.html#bluemix_resource_service_alias_create)</td>
      <td>[bluemix resource service-alias-update](bx_cli.html#bluemix_resource_service_alias_update)</td>
      <td>[bluemix resource service-alias-delete](bx_cli.html#bluemix_resource_service_alias_delete)</td>
    </tr>
    <tr>
      <td>[bluemix resource search](bx_cli.html#bluemix_resource_search)</td>
    </tr>
  </tbody>
</table>


 ## API キーとポリシーを管理するためのコマンド
 {: #bx_commands_iam}
 <table summary="API キーとポリシーを管理するために使用できる bluemix コマンド。">
 <caption>表 3. API キーとポリシーを管理するためのコマンド</caption>
  <thead>
  <th colspan="5">API キーとポリシーを管理するためのコマンド</th>
  </thead>
  <tbody>
  <tr>
   <td>[bluemix iam service-id](bx_cli.html#bluemix_iam_service_id)</td>
   <td>[bluemix iam service-id-create](bx_cli.html#bluemix_iam_service_id_create)</td>
   <td>[bluemix iam service-id-update](bx_cli.html#bluemix_iam_service_id_update)</td>
   <td>[bluemix iam service-id-delete](bx_cli.html#bluemix_iam_service_id_delete)</td>
   <td>[bluemix iam service-ids](bx_cli.html#bluemix_iam_service_ids)</td>
  </tr>
  <tr>
   <td>[bluemix iam api-keys](bx_cli.html#bluemix_iam_api_keys)</td>
   <td>[bluemix iam api-key-create](bx_cli.html#bluemix_iam_api_key_create)</td>
   <td>[bluemix iam api-key-delete](bx_cli.html#bluemix_iam_api_key_delete)</td>
   <td>[bluemix iam api-key-update](bx_cli.html#bluemix_iam_api_key_update)</td>
   <td>[bluemix iam service-api-keys](bx_cli.html#bluemix_iam_service_api_keys)</td>
  </tr>
  <tr>
   <td>[bluemix iam service-api-key](bx_cli.html#bluemix_iam_service_api_key)</td>
   <td>[bluemix iam service-api-key-create](bx_cli.html#bluemix_iam_service_api_key_create)</td>
   <td>[bluemix iam service-api-key-update](bx_cli.html#bluemix_iam_service_api_key_update)</td>
   <td>[bluemix iam service-api-key-delete](bx_cli.html#bluemix_iam_service_api_key_delete)</td>
   <td>[bluemix iam service-policies](bx_cli.html#bluemix_iam_service_policies)</td>
  </tr>
  <tr>
    <td>[bluemix iam service-policy](bx_cli.html#bluemix_iam_service_policy)</td>
    <td>[bluemix iam service-policy-create](bx_cli.html#bluemix_iam_service_policy_create)</td>
    <td>[bluemix iam service-policy-update](bx_cli.html#bluemix_iam_service_policy_update)</td>
    <td>[bluemix iam service-policy-delete](bx_cli.html#bluemix_iam_service_policy_delete)</td>
    <td>[bluemix iam user-policies](bx_cli.html#bluemix_iam_user_policies)</td>
  </tr>
  <tr>
   <td>[bluemix iam user-policy](bx_cli.html#bluemix_iam_user_policy)</td>
   <td>[bluemix iam user-policy-create](bx_cli.html#bluemix_iam_user_policy_create)</td>
   <td>[bluemix iam user-policy-update](bx_cli.html#bluemix_iam_user_policy_update)</td>
   <td>[bluemix iam user-policy-delete](bx_cli.html#bluemix_iam_user_policy_delete)</td>
   <td>[bluemix iam oauth-tokens](bx_cli.html#bluemix_iam_oauth_tokens)</td>
  </tr>
  <tr>
     <td>[bluemix iam dedicated-id-disconnect](bx_cli.html#bluemix_iam_dedicated_id_disconnect)</td>
     <td>[bluemix iam authorization-policy-create](bx_cli.html#bluemix_iam_authorization_policy_create)</td>
     <td>[bluemix iam authorization-policy-delete](bx_cli.html#bluemix_iam_authorization_policy_delete)</td>
     <td>[bluemix iam authorization-policy](bx_cli.html#bluemix_iam_authorization_policy)</td>
     <td>[bluemix iam authorization-policies](bx_cli.html#bluemix_iam_authorization_policies)</td>
  </tr>
  </tbody>
  </table>

 ## CF アプリとアプリ関連ドメイン、経路、および証明書を管理するためのコマンド
 {: #bx_commands_apps}

<table summary="CF アプリとアプリ関連ドメイン、経路、および証明書を管理するために使用できる bluemix コマンド。">
<caption>表 4. CF アプリとアプリ関連ドメイン、経路、および証明書を管理するためのコマンド</caption>
 <thead>
 <th colspan="5">CF アプリとアプリ関連ドメイン、経路、および証明書を管理するためのコマンド</th>
 </thead>
 <tbody>
 <tr>
 <td>[bluemix app push](bx_cli.html#bluemix_app_push)</td>
 <td>[bluemix app list](bx_cli.html#bluemix_app_list)</td>
 <td>[bluemix app show](bx_cli.html#bluemix_app_show)</td>
 <td>[bluemix app delete](bx_cli.html#bluemix_app_delete)</td>
 <td>[bluemix app rename](bx_cli.html#bluemix_app_rename)</td>
 </tr>
 <tr>
 <td>[bluemix app start](bx_cli.html#bluemix_app_start)</td>
 <td>[bluemix app stop](bx_cli.html#bluemix_app_stop)</td>
 <td>[bluemix app restart](bx_cli.html#bluemix_app_restart)</td>
 <td>[bluemix app restage](bx_cli.html#bluemix_app_restage)</td>
 <td>[bluemix app instance-restart](bx_cli.html#bluemix_app_instance_restart)</td>
 </tr>
 <tr>
 <td>[bluemix app events](bx_cli.html#bluemix_app_events)</td>
 <td>[bluemix app files](bx_cli.html#bluemix_app_files)</td>
 <td>[bluemix app logs](bx_cli.html#bluemix_app_logs)</td>
 <td>[bluemix app env](bx_cli.html#bluemix_app_env)</td>
 <td>[bluemix app env-set](bx_cli.html#bluemix_app_env_set)</td>
 </tr>
 <tr>
 <td>[bluemix app env-unset](bx_cli.html#bluemix_app_env_unset)</td>
 <td>[bluemix app stacks](bx_cli.html#bluemix_app_stacks)</td>
 <td>[bluemix app stack-show](bx_cli.html#bluemix_app_stack_show)</td>
 <td>[bluemix app manifest-create](bx_cli.html#bluemix_app_manifest_create)</td>
 <td>[bluemix app domain-cert](bx_cli.html#bluemix_app_domain_cert)</td>
 </tr>
 <tr>
  <td>[bluemix app domain-cert-add](bx_cli.html#bluemix_app_domain_cert_add)</td>
  <td>[bluemix app domain-cert-remove](bx_cli.html#bluemix_app_domain_cert_remove)</td>
  <td>[bluemix app domains](bx_cli.html#bluemix_app_domains)</td>
  <td>[bluemix app domain-create](bx_cli.html#bluemix_app_domain_create)</td>
  <td>[bluemix app domain-delete](bx_cli.html#bluemix_app_domain_delete)</td>
 </tr>
 <tr>
  <td>[bluemix app shared-domain-create](bx_cli.html#bluemix_app_shared_domain_create)</td>
  <td>[bluemix app shared-domain-delete](bx_cli.html#bluemix_app_shared_domain_delete)</td>
  <td>[bluemix app routes](bx_cli.html#bluemix_app_routes)</td>
  <td>[bluemix app route-check](bx_cli.html#bluemix_app_route_check)</td>
  <td>[bluemix app route-map](bx_cli.html#bluemix_app_route_map)</td>
 </tr>
 <tr>
  <td>[bluemix app route-unmap](bx_cli.html#bluemix_app_route_unmap)</td>
  <td>[bluemix app route-create](bx_cli.html#bluemix_app_route_create)</td>
  <td>[bluemix app route-delete](bx_cli.html#bluemix_app_route_delete)</td>
  <td>[bluemix app orphaned-routes-delete](bx_cli.html#bluemix_app_orphaned_routes_delete)</td>
  <td></td>
 </tr>
  </tbody>
 </table>

 ## {{site.data.keyword.Bluemix_notm}} サービスを管理するためのコマンド
 {: #bx_commands_services}

<table summary="{{site.data.keyword.Bluemix_notm}} サービスを管理するために使用できる bluemix コマンド">
<caption>表 5. {{site.data.keyword.Bluemix_notm}} サービスを管理するためのコマンド</caption>
 <thead>
 <th colspan="5">{{site.data.keyword.Bluemix_notm}} サービスを管理するためのコマンド</th>
 </thead>
 <tbody>
 <tr>
 <td>[bluemix service offerings](bx_cli.html#bluemix_service_offerings)</td>
 <td>[bluemix service list](bx_cli.html#bluemix_service_list)</td>
 <td>[bluemix service show](bx_cli.html#bluemix_service_show)</td>
 <td>[bluemix service create](bx_cli.html#bluemix_service_create)</td>
 <td>[bluemix service update](bx_cli.html#bluemix_service_update)</td>
 </tr>
 <tr>
 <td>[bluemix service delete](bx_cli.html#bluemix_service_delete)</td>
 <td>[bluemix service rename](bx_cli.html#bluemix_service_rename)</td>
 <td>[bluemix service bind](bx_cli.html#bluemix_service_bind)</td>
 <td>[bluemix service unbind](bx_cli.html#bluemix_service_unbind)</td>
 <td>[bluemix service key-create](bx_cli.html#bluemix_service_key_create)</td>
 </tr>
 <tr>
 <td>[bluemix service key-delete](bx_cli.html#bluemix_service_key_delete)</td>
 <td>[bluemix service keys](bx_cli.html#bluemix_service_keys)</td>
 <td>[bluemix service key-show](bx_cli.html#bluemix_service_key_show)</td>
 <td>[bluemix service user-provided-create](bx_cli.html#bluemix_service_user_provided_create)</td>
 <td>[bluemix service user-provided-update](bx_cli.html#bluemix_service_user_provided_update)</td>
 </tr>
  </tbody>
 </table>


 ## カタログ、プラグイン、および請求処理の設定を管理するためのコマンド
 {: #bx_commands_settings}

<table summary="{{site.data.keyword.Bluemix_notm}} カタログ、プラグイン、請求、およびセキュリティー設定を管理するために使用できる bluemix コマンド">
<caption>表 6. {{site.data.keyword.Bluemix_notm}} カタログ、プラグイン、請求、およびセキュリティー設定を管理するためのコマンド</caption>
 <thead>
 <th colspan="5">{{site.data.keyword.Bluemix_notm}} カタログ、プラグイン、請求、およびセキュリティー設定を管理するためのコマンド</th>
 </thead>
 <tbody>
 <tr>
  <td>[bluemix catalog search](bx_cli.html#bluemix_catalog_search)</td>
  <td>[bluemix catalog entry](bx_cli.html#bluemix_catalog_entry)</td>
  <td>[bluemix catalog entry-create](bx_cli.html#bluemix_catalog_entry_create)</td>
  <td>[bluemix catalog entry-update](bx_cli.html#bluemix_catalog_entry_update)</td>
  <td>[bluemix catalog entry-delete](bx_cli.html#bluemix_catalog_entry_delete)</td>
 </tr>
 <tr>
  <td>[bluemix catalog entry-visibility](bx_cli.html#bluemix_catalog_entry_visibility)</td>
  <td>[bluemix catalog service-marketplace](bx_cli.html#bluemix_catalog_service_marketplace)</td>
  <td>[bluemix catalog entry-visibility-set](bx_cli.html#bluemix_catalog_entry_visibility_set)</td>
  <td>[bluemix catalog templates](bx_cli.html#bluemix_catalog_templates)</td>
  <td>[bluemix catalog template](bx_cli.html#bluemix_catalog_template)</td>
 </tr>
 <tr>
  <td>[bluemix catalog template-run](bx_cli.html#bluemix_catalog_template_run)</td>
  <td>[bluemix catalog locations](bx_cli.html#bluemix_catalog_locations)</td>
  <td>[bluemix catalog runtime](bx_cli.html#bluemix_catalog_runtime)</td>
  <td>[bluemix catalog runtimes](bx_cli.html#bluemix_catalog_runtimes)</td>
  <td>[bluemix plugin repos](bx_cli.html#bluemix_plugin_repos)</td>
</tr>
<tr>
  <td>[bluemix plugin repo-add](bx_cli.html#bluemix_plugin_repo_add)</td>
  <td>[bluemix plugin repo-remove](bx_cli.html#bluemix_plugin_repo_remove)</td>
  <td>[bluemix plugin repo-plugins](bx_cli.html#bluemix_plugin_repo_plugins)</td>
  <td>[bluemix plugin repo-plugin](bx_cli.html#bluemix_plugin_repo_plugin)</td>
  <td>[bluemix plugin list](bx_cli.html#bluemix_plugin_list)</td>
</tr>
<tr>
  <td>[bluemix plugin install](bx_cli.html#bluemix_plugin_install)</td>
  <td>[bluemix plugin uninstall](bx_cli.html#bluemix_plugin_uninstall)</td>
  <td>[bluemix plugin update](bx_cli.html#bluemix_plugin_update)</td>
  <td>[bluemix billing account-usage](bx_cli.html#bluemix_billing_account_usage)</td>
  <td>[bluemix billing org-usage](bx_cli.html#bluemix_billing_org_usage)</td>
</tr>
<tr>
  <td>[bluemix billing resource-group-usage](bx_cli.html#bluemix_resource_group_usage)</td>
  <td>[bluemix billing resource-instances-usage](bx_cli.html#bluemix_resource_instances_usage)</td>
 </tr>
 </tbody>
 </table>

## bluemix help
{: #bluemix_help}
{{site.data.keyword.Bluemix_notm}} CLI の第 1 レベルの組み込みコマンドおよびサポートされる名前空間に関する一般ヘルプを表示するか、または、特定の組み込みコマンドまたは名前空間に関するヘルプを表示します。

```
bluemix help [COMMAND|NAMESPACE]
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>COMMAND|NAMESPACE (オプション)</dt>
   <dd>ヘルプを表示する対象のコマンドまたは名前空間。 指定されない場合、{{site.data.keyword.Bluemix_notm}} CLI の一般ヘルプが表示されます。</dd>
   </dl>



<strong>例</strong>:

{{site.data.keyword.Bluemix_notm}} CLI の一般ヘルプを表示します。

```
bluemix help
```

`info` コマンドのヘルプを表示します。

```
bluemix help info
```



## bluemix api
{: #bluemix_api}
{{site.data.keyword.Bluemix_notm}} API エンドポイントを設定または表示します。

```
bluemix api [API_ENDPOINT] [--unset] [--skip-ssl-validation]
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>API_ENDPOINT (オプション)</dt>
   <dd>ターゲットの API エンドポイント (例えば `https://api.chinabluemix.net`)。 *API_ENDPOINT* オプションと `--unset` オプションのどちらも指定されない場合、現行 API エンドポイントが表示されます。</dd>
   <dt>--unset (オプション)</dt>
   <dd>API エンドポイント設定を削除します。</dd>
   <dt>--skip-ssl-validation (オプション)</dt>
   <dd>HTTP 要求の SSL 検証をバイパスします。</dd>
   </dl>
<strong>例</strong>:

API エンドポイントを api.chinabluemix.net に設定します。

```
bluemix api api.chinabluemix.net
```

```
bluemix api https://api.chinabluemix.net --skip-ssl-validation
```

現行 API エンドポイントを表示します。

```
bluemix api
```

API エンドポイントを設定解除します。

```
bluemix api --unset
```

## bluemix config
{: #bluemix_config}


構成ファイルにデフォルト値を書き込みます。

```
bluemix config --http-timeout TIMEOUT_IN_SECONDS | --trace (true|false|path/to/file) | --color (true|false) | --locale (LOCALE|CLEAR) | --check-version (true|false)
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>--http-timeout <i>TIMEOUT_IN_SECONDS</i></dt>
   <dd>HTTP 要求のタイムアウト値。 デフォルト値は 60 秒です。</dd>
   <dt>--trace true|false|<i>path-to-file</i></dt>
   <dd>端末または指定されたファイルへの HTTP 要求をトレースします。</dd>
   <dt>--color true|false</dt>
   <dd>カラー出力を使用可能または使用不可にします。 カラー出力はデフォルトで使用可能に設定されています。</dd>
   <dt>--locale <i>LOCALE|CLEAR</i></dt>
   <dd>デフォルト・ロケールを設定します。 LOCALE  が <i>CLEAR</i> の場合は、前のロケールが削除されます。</dd>
   <dt>--check-version true|false</dt>
   <dd>CLI バージョン・チェックを使用可能または使用不可にします。</dd>
   </dl>

一度に指定できるのは、これらのオプションの 1 つだけです。

<strong>例</strong>:

次のように、HTTP 要求タイムアウトを 30 秒に設定します。

```
bluemix config --http-timeout 30
```

次のように、HTTP 要求のトレース出力を使用可能にします。

```
bluemix config --trace true
```

次のように、指定されたファイル */home/usera/my_trace* への HTTP 要求をトレースします。

```
bluemix config --trace /home/usera/my_trace
```

次のように、カラー出力を使用不可にします。

```
bluemix config --color false
```

次のように、ロケールを zh_Hans に設定します。

```
bluemix config --locale zh_Hans
```

次のように、ロケール設定をクリアします。

```
bluemix config --locale CLEAR
```



## bluemix info
{: #bluemix_info}

基本的な {{site.data.keyword.Bluemix_notm}} 情報を表示します。これには、現行領域、クラウド・コントローラーのバージョン、および、いくつかの有用なエンドポイント (例えば、ログイン用のエンドポイントや、アクセス・トークン交換用のエンドポイントなど) が含まれます。

```
bluemix info
```

<strong>前提条件</strong>: エンドポイント


## bluemix cf
{: #bluemix_cf}

組み込み CF CLI を呼び出します

```
bluemix [-q, --quiet] cf COMMAND...
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-q, --quiet</dt>
  <dd>「cf コマンドの呼び出し中...」というメッセージをオフにします</dd>
</dl>

<strong>例</strong>:

cf アプリをリストします

```
bluemix cf apps
```

「cf コマンドの呼び出し中...」というメッセージを表示せずに cf サービスをリストします

```
bluemix -q cf services
```


## bluemix login
{: #bluemix_login}

ユーザーをログインします。

```
bluemix login [-a API_ENDPOINT] [--sso] [-u USERNAME] [-p PASSWORD] [--apikey KEY | @KEY_FILE] [--no-iam] [-c ACCOUNT_ID] [-g RESOURCE_GROUP] [-o ORG] [-s SPACE]
```

<strong>前提条件</strong>: なし

<!-- staging comment for Atlas 45: might need prereq for federated ID/SSO option unless we expect them to just view the details from the cf login command -->

<strong>コマンド・オプション</strong>:
<dl>
  <dt> -a <i>API_ENDPOINT</i> (オプション)</dt>
  <dd> API エンドポイント (例: api.ng.bluemix.net)</dd>
  <dt> --apikey <i>API_KEY または @API_KEY_FILE_PATH</i>
  <dd> API キーの内容、または @ で示された API キー・ファイルのパス</dd>
  <dt> --sso (オプション) </dt>
  <dd> ワンタイム・パスコードを使用してログインします </dd>
  <dt> -u <i>USERNAME</i> (オプション)</dt>
  <dd> ユーザー名</dd>
  <dt> -p <i>PASSWORD</i> (オプション)</dt>
  <dd> パスワード</dd>
  <dt> -c <i>ACCOUNT_ID</i> (オプション) </dt>
  <dd> ターゲット・アカウントの ID</dd>
  <dt> -g <i>RESOURCE_GROUP</i> (オプション) </dt>
  <dd> ターゲット・リソース・グループの名前</dd>
  <dt> -o <i>ORG</i> (オプション)</dt>
  <dd> ターゲット組織の名前 (非推奨。'bluemix target -o ORG' を使用のこと)</dd>
  <dt> -s <i>SPACE</i> (オプション) </dt>
  <dd> ターゲット・スペースの名前 (非推奨。'bluemix target -s SPACE' を使用のこと)</dd>
  <dt> --no-iam </dt>
  <dd> パブリック IAM の代わりにログイン・サーバーでの認証を強制します</dd>
  <dt> --skip-ssl-validation (オプション) </dt>
  <dd> HTTP 要求の SSL 検証をバイパスします。 このオプションは推奨されません。</dd>
</dl>

<strong>例</strong>:

#### 対話式ログイン

```
bluemix login
```

以下のように、ユーザー名とパスワードを使用してログインし、ターゲットのアカウント、組織、およびスペースを設定します。

```
bluemix login -u username -p password -c MyAccountID -o MyOrg -s MySpace
```

ワンタイム・パスコードを使用してログインし、ターゲット・アカウント、組織、およびスペースを設定します

```
bluemix login --sso -c MyAccountID -o MyOrg -s MySpace
```

API キーを使用してログインし、ターゲットを設定します。

#### API キーにアカウントが関連付けられている

```
bluemix login --apikey api-key-string -o MyOrg -s MySpace
```

```
bluemix login --apikey @filename -o MyOrg -s MySpace
```

#### API キーにアカウントが関連付けられていない

```
bluemix login --apikey api-key-string -c MyAccountID -o MyOrg -s MySpace
```

```
bluemix login --apikey @fileName -c MyAccountID -o MyOrg -s MySpace
```

<strong>注:</strong> API キーに、関連付けられたアカウントがある場合、別のアカウントへの切り替えは許可されません。

#### ワンタイム・パスコードを使用する

```
bluemix login -u UserID --sso
```

すると、CLI は以下のように URL リンクを提供し、パスコードの入力を要求します。
```
One Time Code (Get one at https://URL_Link_To_Obtain_Passcode):
```

ブラウザーでこのリンクを開くと、パスコードを取得するための案内が表示されます。 提供されたパスコードをコンソールに入力するとログインできます。

## bluemix logout
{: #bluemix_logout}

ユーザーをログアウトします。

```
bluemix logout
```

<strong>前提条件</strong>: なし

## bluemix regions
{: #bluemix_regions}

{{site.data.keyword.Bluemix_notm}} のすべての地域の情報を表示します。

```
bluemix regions
```

<strong>前提条件</strong>: エンドポイント


## bluemix target
{: #bluemix_target}


ターゲット・アカウント、地域、組織、またはスペースを設定するか表示します。

```
bluemix target [-r REGION_NAME] [-c ACCOUNT_ID] [-g RESOURCE_GROUP] [--cf] [-o ORG] [-s SPACE]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>-r <i>REGION_NAME</i> (オプション)</dt>
   <dd>切り替え先の地域の名前。例えば、「us-south」または「eu-gb」など。</dd>
   <dt>-c <i>ACCOUNT_ID</i> (オプション)</dt>
   <dd>ターゲットとなるアカウントの ID。</dd>
   <dt>-g <i>RESOURCE_GROUP</i> (オプション)</dt>
   <dd>リソース・グループの名前。</dd>
   <dt>--cf</dt>
   <dd>ターゲットの組織およびスペースを対話式に選択します</dd>
   <dt>-o <i>ORG_NAME</i> (オプション)</dt>
   <dd>ターゲットとなる組織の名前。</dd>
   <dt>-s <i>SPACE_NAME</i> (オプション)</dt>
   <dd>ターゲットとなるスペースの名前。</dd>
   </dl>
どのオプションも指定されていない場合、現行のアカウント、地域、組織、およびスペースが表示されます。

<strong>例</strong>:

現行のアカウント、組織、およびスペースを設定します。

```
bluemix target -c MyAccountID -o MyOrg -s MySpace
```

新しい地域に切り替えます。

```
bluemix target -r eu-gb
```

現行のアカウント、地域、組織、およびスペースを表示します。

```
bluemix target
```

## bluemix update
{: #bluemix_update}

CLI を最新バージョンに更新します。

```
bluemix update [-f]
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-f</dt>
  <dd>確認を求めずに更新を強制します。 root 権限が必要です。</dd>
</dl>

### bluemix account orgs
{: #bluemix_account_orgs}

すべての組織をリストします。

```
bluemix account orgs [-r REGION] [--guid]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>-r <i>REGION</i> (オプション)</dt>
   <dd>どの地域の組織情報を表示するかを指定します。 'all' に設定された場合は、すべての地域のすべての組織がリストされます。</dd>
   <dt>--guid (オプション)</dt>
   <dd>組織の GUID を表示します。</dd>
   </dl>

<strong>例</strong>:

地域 `us-south` 内のすべての組織を、GUID の
出力と共にリストします。

```
bluemix account orgs -r us-south --guid
```

## bluemix account org
{: #bluemix_account_org}

指定された組織の情報を表示します。

```
bluemix account org ORG_NAME [--guid]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>ORG_NAME (必須)</dt>
   <dd>組織の名前。</dd>
   <dt>--guid (オプション)</dt>
   <dd>組織の GUID を表示します。</dd>
   </dl>

<strong>例</strong>:

組織 `IBM`
の情報を、GUID の出力と共に表示します

```
bluemix account org IBM --guid
```


## bluemix account org-create
{: #bluemix_account_org_create}

新しい組織を作成します。 この操作は、アカウントの所有者のみが実行できます。

```
bluemix account org-create ORG_NAME [-f]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>ORG_NAME (必須)</dt>
   <dd>作成される組織の名前。</dd>
   <dt>-f</dt>
   <dd>確認を求めずに作成を強制します。</dd>
   </dl>

<strong>例</strong>:

名前が `IBM` という組織を作成します。

```
bluemix account org-create IBM
```

## bluemix account org-replicate
{: #bluemix_account_org_replicate}

現在の地域から別の地域に組織を複製します。

```
bluemix account org-replicate ORG_NAME REGION_NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>ORG_NAME (必須)</dt>
   <dd>複製する既存の組織の名前。</dd>
   <dt>REGION_NAME (必須)</dt>
   <dd>複製された組織をホストする地域の名前。</dd>
   </dl>

<strong>例</strong>:

組織 `myorg` を地域 `eu-gb` に複製します。

```
bluemix account org-replicate myorg eu-gb
```


## bluemix account org-rename
{: #bluemix_account_org_rename}

組織の名前を変更します。 この操作は、組織の管理者のみが実行できます。

```
bluemix account org-rename OLD_ORG_NAME NEW_ORG_NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>OLD_ORG_NAME (必須)</dt>
   <dd>名前を変更する組織の古い名前。</dd>
   <dt>NEW_ORG_NAME (必須)</dt>
   <dd>名前を変更する組織の新しい名前。</dd>
   </dl>


## bluemix account spaces
{: #bluemix_account_spaces}

すべてのスペースをリストします

```
bluemix account spaces [-o ORG_NAME] [-r REGION-NAME]
```

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>-o</dt>
   <dd>組織名。 指定された組織の下のスペースをリストします。 未指定の場合、デフォルトは現行組織です。</dd>
   <dt>-r</dt>
   <dd>地域名。 指定した地域の下のスペースをリストします。 未指定の場合、デフォルトは現行地域です。</dd>
   </dl>



## bluemix account space
{: #bluemix_account_space}

このコマンドの機能とオプションは [cf space ![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/space.html){: new_window} コマンドと同じです。


## bluemix account space-create
{: #bluemix_account_space_create}

このコマンドの機能とオプションは [cf create-space![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/create-space.html){: new_window} コマンドと同じです。


## bluemix account space-rename
{: #bluemix_account_space_rename}


このコマンドの機能とオプションは [cf rename-space![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/rename-space.html){: new_window} コマンドと同じです。


## bluemix account space-delete
{: #bluemix_account_space_delete}


このコマンドの機能とオプションは [cf delete-space![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/delete-space.html){: new_window} コマンドと同じです。

## bluemix account org-users
{: #bluemix_account_org_users}

指定された組織内のユーザーを役割別に表示します

```
bluemix account org-users ORG_NAME [-a]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
<dt>ORG_NAME (必須)</dt>
<dd>組織の名前。</dd>
<dt>-a (オプション)</dt>
<dd>指定された組織内のすべてのユーザーを、役割別にグループ化せずにリストします。</dd>
</dl>

## bluemix account org-user-add
{: #bluemix_account_org_user_add}

組織にユーザーを追加します (組織管理者が必要)。

```
 bluemix account org-user-add USER_NAME ORG
```

## bluemix account org-user-remove
{: #bluemix_account_org_user_remove}

組織からユーザーを削除します (組織管理者またはユーザー本人のみ)

```
   bluemix account org-user-remove USER_NAME ORG [-f, --force]
```

<strong>コマンド・オプション</strong>:
<dl>
<dt>--force, -f</dt>
<dd>確認なしで削除を強制します。</dd>
</dl>

## bluemix account org-roles
{: #bluemix_account_org_roles}

現行ユーザーのすべての組織の役割を取得します

```
bluemix account org-roles [-u USER_ID]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
  <dl>
   <dt>-u</dt>
   <dd>ユーザー ID。 指定しない場合、現行ユーザーがデフォルトで使用されます。</dd>
  </dl>

## bluemix account org-role-set
{: #bluemix_account_org_role_set}

組織の役割をユーザーに割り当てます。 この操作は、組織の管理者のみが実行できます。

```
bluemix account org-role-set USER_NAME ORG_NAME ORG_ROLE
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
  <dl>
   <dt>USER_NAME (必須)</dt>
   <dd>割り当てられるユーザーの名前。</dd>
   <dt>ORG_NAME (必須)</dt>
   <dd>このユーザーの割り当て先の組織の名前。</dd>
   <dt>ORG_ROLE (必須)</dt>
   <dd>このユーザーの割り当て先の組織内での役割の名前。 以下に例を示します。
   <ul>
   <li>OrgManager: この役割は、ユーザーの招待と管理、プランの選択と変更、支払上限の設定を行います。</li>
   <li>BillingManager: この役割は、請求アカウントと支払い情報の作成および管理を行えます。</li>
   <li>OrgAuditor: この役割は、組織の情報とレポートに読み取りアクセスだけが可能です。</li>
   </ul>
   </dd>
  </dl>

<strong>例</strong>:

ユーザー `Mary` を組織 `IBM` に役割 `OrgManager` として割り当てるには、次のように指定します。

```
bluemix account org-role-set Mary IBM OrgManager
```
<!-- Begin Staging URL vs Prod URL -->
**注**: 組織/スペースの役割は CLI を使用して設定できますが、その他の許可を設定したい場合は、UI を使用する必要があります。 詳細については、[ユーザー・アクセスの割り当て](/docs/iam/assignaccess.html#assignaccess)を参照してください。
<!-- Begin Staging URL vs Prod URL -->

## bluemix account org-role-unset
{: #bluemix_account_org_role_unset}

組織の役割をユーザーから削除します。 この操作は、組織の管理者のみが実行できます。

```
bluemix account org-role-unset USER_NAME ORG_NAME ORG_ROLE
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>USER_NAME (必須)</dt>
   <dd>削除されるユーザーの名前。</dd>
   <dt>ORG_NAME (必須)</dt>
   <dd>このユーザーの削除元の組織の名前。</dd>
   <dt>ORG_ROLE (必須)</dt>
   <dd>このユーザーの削除元の組織内での役割の名前。 以下に例を示します。
   <ul>
   <li>OrgManager: この役割は、ユーザーの招待と管理、プランの選択と変更、支払上限の設定を行います。</li>
   <li>BillingManager: この役割は、請求アカウントと支払い情報の作成および管理を行えます。</li>
   <li>OrgAuditor: この役割は、組織の情報とレポートに読み取りアクセスだけが可能です。</li>
   </ul>
   </dd>
    </dl>

<strong>例</strong>:

ユーザー `Mary` を組織 `IBM` の役割 `OrgManager` から削除するには、次のように指定します。

```
bluemix account org-role-unset Mary IBM OrgManager
```

## bluemix account space-users
{: #bluemix_account_space_users}

指定されたスペース内のユーザーを役割別に表示します

```
bluemix account space-users ORG_NAME SPACE_NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>ORG_NAME (必須)</dt>
   <dd>組織の名前。</dd>
   <dt>SPACE_NAME (必須)</dt>
   <dd>スペースの名前。</dd>
   </dl>


## bluemix account space-role-set
{: #bluemix_account_space_role_set}

スペースの役割をユーザーに割り当てます。 この操作は、スペースの管理者のみが実行できます。

```
bluemix account space-role-set USER_NAME ORG_NAME SPACE_NAME SPACE_ROLE
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>USER_NAME (必須)</dt>
   <dd>割り当てられるユーザーの名前。</dd>
   <dt>ORG_NAME (必須)</dt>
   <dd>このユーザーの割り当て先の組織の名前。</dd>
   <dt>SPACE_NAME (必須)</dt>
   <dd>このユーザーの割り当て先のスペースの名前。</dd>
   <dt>SPACE_ROLE (必須)</dt>
   <dd>このユーザーの割り当て先のスペース内での役割の名前。 以下に例を示します。
   <ul>
   <li>SpaceManager: この役割は、ユーザーの招待と管理を行い、特定のスペースに対してフィーチャーを有効にします。</li>
   <li>SpaceDeveloper: この役割は、アプリとサービスを作成して管理し、ログとレポートを表示します。</li>
   <li>SpaceAuditor: この役割は、ログ、レポート、スペースの設定を表示できます。</li>
   </ul></dd>
    </dl>

<strong>例</strong>:

ユーザー `Mary` を組織 `IBM` およびスペース `Cloud` に役割 `SpaceManager` として割り当てるには、次のように指定します。

```
bluemix account space-role-set Mary IBM Cloud SpaceManager
```

## bluemix account space-role-unset
{: #bluemix_account_space_role_unset}

スペースの役割をユーザーから削除します。 この操作は、スペースの管理者のみが実行できます。

```
bluemix account space-role-unset USER_NAME ORG_NAME SPACE_NAME SPACE_ROLE
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>USER_NAME (必須)</dt>
   <dd>削除されるユーザーの名前。</dd>
   <dt>ORG_NAME (必須)</dt>
   <dd>このユーザーの削除元の組織の名前。</dd>
   <dt>SPACE_NAME (必須)</dt>
   <dd>このユーザーの削除元のスペースの名前。</dd>
   <dt>SPACE_ROLE (必須)</dt>
   <dd>このユーザーの削除元のスペース内での役割の名前。 以下に例を示します。
   <ul>
   <li>SpaceManager: この役割は、ユーザーの招待と管理を行い、特定のスペースに対してフィーチャーを有効にします。</li>
   <li>SpaceDeveloper: この役割は、アプリとサービスを作成して管理し、ログとレポートを表示します。</li>
   <li>SpaceAuditor: この役割は、ログ、レポート、スペースの設定を表示できます。</li>
   </ul></dd>
    </dl>


<strong>例</strong>:

ユーザー `Mary` を組織 `IBM` と、役割 `SpaceManager` としてのスペース `Cloud` から削除するには、次のように指定します。

```
bluemix account space-role-unset Mary IBM Cloud SpaceManager
```

## bluemix account list
{: #bluemix_account_list}

現行ユーザーのすべてのアカウントをリストします

```
bluemix account list
```

<strong>前提条件</strong>: エンドポイント、ログイン


## bluemix account org-account
{: #bluemix_account_org_account}

指定された組織のアカウントを表示します (組織のユーザーが必要)。

```
bluemix account org-account ORG_NAME [--guid]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>--guid (オプション)</dt>
  <dd>アカウント ID のみを表示します</dd>
</dl>


## bluemix account users
{: #bluemix_account_users}

アカウントに関連付けられているユーザーを表示します。 この操作は、アカウントの所有者のみが実行できます。

```
bluemix account users
```

## bluemix account user-delete
{: #bluemix_account_user_delete}

現行アカウントからユーザーを削除します (アカウント所有者のみ)

```
bluemix account user-delete USERNAME [-c ACCOUNT_ID] [-f]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
<dt>USERNAME (必須)</dt>
<dd>ユーザー名</dd>
<dt>-c ACCOUNT_ID</dt>
<dd>アカウント ID。 指定しない場合、現行アカウントがデフォルトで使用されます。</dd>
<dt>--force、-f (オプション)</dt>
<dd>確認なしで削除を強制します。</dd>
</dl>

## bluemix account user-invite
{: #bluemix_account_user_invite}

ユーザーをアカウントに招待します (アカウント管理者)

```
bluemix account user-invite USER_EMAIL
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
   <dt>USER_EMAIL (必須)</dt>
   <dd>招待されるユーザーの E メール。</dd>
</dl>


## bluemix account user-reinvite
{: #bluemix_account_user_reinvite}

ユーザーに招待を再送信します (アカウント管理者)

```
bluemix account user-reinvite USER_EMAIL
```
<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
   <dt>USER_EMAIL (必須)</dt>
   <dd>再度招待されるユーザーの E メール。</dd>
</dl>

## bluemix iam access-groups
{: #bluemix_iam_access_groups}

現行アカウントのアクセス・グループをリストします

```
bluemix iam access-groups [-u USER_NAME | -s SERVICE_ID_NAME]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-u</dt>
  <dd>ユーザーが所属するアクセス・グループをリストします。このフラグと '-s' を同時に指定することはできません。</dd>
  <dt>-s</dt>
  <dd>サービス ID が所属するアクセス・グループをリストします。このフラグと '-u' を同時に指定することはできません。</dd>
</dl>

<strong>例</strong>:

すべてのアクセス・グループをリストします

```
bluemix iam access-groups
```

## bluemix iam access-group
{: #bluemix_iam_access_group}

アクセス・グループの詳細を表示します

```
bluemix iam access-group GROUP_NAME [--id]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-id</dt>
  <dd>ID のみを表示します</dd>
</dl>

<strong>例</strong>:

アクセス・グループ `example_group` の詳細を表示します。

```
bluemix iam access-group example_group
```

## bluemix iam access-group-create
{: #bluemix_iam_access_group_create}

アクセス・グループを作成します

```
bluemix iam access-group-create GROUP_NAME [-d, --description DESCRIPTION]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-d, --description</dt>
  <dd>アクセス・グループの説明</dd>
</dl>

<strong>例</strong>:

アクセス・グループ `example_group` を作成します。

```
bluemix iam access-group-create example_group -d "example access group"
```

## bluemix iam access-group-update
{: #bluemix_iam_access_group_update}

アクセス・グループを更新します

```
bluemix iam access-group-update GROUP_NAME [-n, --name NEW_NAME] [-d, --description NEW_DESCRIPTION] [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-n, --name</dt>
  <dd>新規アクセス・グループ名</dd>
  <dt>-d, --description</dt>
  <dd>新規説明</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに更新を強制します</dd>
</dl>

<strong>例</strong>:

アクセス・グループ `example_group` を `hello_world_group` に名前変更します。

```
bluemix iam access-group-update example_group --name "hello_world_group"
```

## bluemix iam access-group-delete
{: #bluemix_iam_access_group_delete}

アクセス・グループを削除します

```
bluemix iam access-group-delete GROUP_NAME [-f, --force] [-r, --recursive]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>確認なしで削除を強制します</dd>
  <dt>-r, --recursive</dt>
  <dd>アクセス・グループとそのメンバーを削除します</dd>
</dl>

<strong>例</strong>:

アクセス・グループ `example_group` を削除します。

```
bluemix iam access-group-delete example_group --force
```

## bluemix iam access-group-users
{: #bluemix_iam_access_group_users}

アクセス・グループ内のユーザーをリストします

```
bluemix iam access-group-users GROUP_NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

アクセス・グループ `example_group` 内のすべてのユーザーをリストします。

```
bluemix iam access-group-users example_group
```

## bluemix iam access-group-user-add
{: #bluemix_iam_access_group_user_add}

アクセス・グループにユーザーを追加します

```
bluemix iam access-group-user-add GROUP_NAME USER_NAME [USER_NAME2...]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

ユーザー `name@example.com` をアクセス・グループ `example_group` に追加します。

```
bluemix iam access group-user-add example_group name@example.com
```

## bluemix iam access-group-user-remove
{: #bluemix_iam_access_group_user_remove}

アクセス・グループからユーザーを削除します

```
bluemix iam access-group-user-remove GROUP_NAME USER_NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

ユーザー `name@example.com` をアクセス・グループ `example_group` から削除します。

```
bluemix iam access-group-user-remove example_group name@example.com
```

## bluemix iam access-group-user-purge
{: #bluemix_iam_access_group_user_purge}

すべてのアクセス・グループからユーザーを削除します

```
bluemix iam access-group-user-purge USER_NAME [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>確認を求めずに削除します</dd>
</dl>

<strong>例</strong>:

ユーザー `name@example.com` をすべてのアクセス・グループから削除します。

```
bluemix iam access-group-user-purge name@example.com -f
```

## bluemix iam access-group-service-ids
{: #bluemix_iam_access_group_service_ids}

アクセス・グループ内のサービス ID をリストします

```
bluemix iam access-group-service-ids GROUP_NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

アクセス・グループ `example_group` 内のすべてのサービス ID をリストします。

```
bluemix iam access-group-service-ids example_group
```

## bluemix iam access-group-service-id-add
{: #bluemix_iam_access_group_service_id_add}

サービス ID をアクセス・グループに追加します

```
bluemix iam access-group-service-id-add GROUP_NAME SERVICE_ID_NAME [SERVICE_ID_NAME2...]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

サービス ID `example-service` をアクセス・グループ `example_group` に追加します。

```
bluemix iam access-group-service-id-add example_group example-service
```

## bluemix iam access-group-service-id-remove
{: #bluemix_iam_access_group_service_id_remove}

アクセス・グループからサービス ID を削除します

```
bluemix iam access-group-service-id-remove GROUP_NAME SERVICE_ID_NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

サービス ID `example-service` をアクセス・グループ `example_group` から削除します。

```
bluemix iam access-group-service-id-remove example_group example-service
```

## bluemix iam access-group-service-id-purge
{: #bluemix_iam_access_group_service_id_purge}

サービス ID をすべてのアクセス・グループから削除します

```
bluemix iam access-group-service-id-purge SERVICE_ID_NAME [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>確認を求めずに削除します</dd>
</dl>

<strong>例</strong>:

サービス ID `example-service` をすべてのアクセス・グループからから削除します。

```
bluemix iam access-group-service-id-purge example --force
```

## bluemix iam access-group-policies
{: #bluemix_iam_access_group_policies}

アクセス・グループのポリシーをリストします

```
bluemix iam access-group-policies GROUP_NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

アクセス・グループ `example_group` のすべてのポリシーをリストします。

```
bluemix iam access-group-policies example_group
```

## bluemix iam access-group-policy
{: #bluemix_iam_access_group_policy}

アクセス・グループ・ポリシーの詳細を表示します

```
bluemix iam access-group-policy GROUP_NAME POLICY_ID
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

アクセス・グループ `example_group` のポリシー `51b9717e-76b0-4f6a-bda7-b8132431f926` の詳細を表示します

```
bluemix iam access-group-policy example_group 51b9717e-76b0-4f6a-bda7-b8132431f926
```

## bluemix iam access-group-policy-create
{: #bluemix_iam_access_group_policy_create}

アクセス・グループ・ポリシーを作成します

```
bluemix iam access-group-policy-create GROUP_NAME {-f, --file @JSON_FILE | --roles ROLE_NAME1,ROLE_NAME2... [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]}
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-f, --file</dt>
  <dd>ポリシー定義の JSON ファイル</dd>
  <dt>-roles</dt>
  <dd>ポリシー定義の役割名。 特定のサービスの、サポートされる役割については、「bluemix iam roles --service SERVICE_NAME」を実行してください。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-service-name</dt>
  <dd>ポリシー定義のサービス名。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-service-instance</dt>
  <dd>ポリシー定義のサービス・インスタンス。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-region</dt>
  <dd>ポリシー定義の地域。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-resource-type</dt>
  <dd>ポリシー定義のリソース・タイプ。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-resource</dt>
  <dd>ポリシー定義のリソース。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-resource-group-name</dt>
  <dd>リソース・グループの名前。 このオプションは、「-f, --file」および「--resource-group-id」と同時に指定することはできません。</dd>
  <dt>-resource-group-id</dt>
  <dd>リソース・グループの ID。 このオプションは、「-f, --file」および「--resource-group-name」と同時に指定することはできません。</dd>
</dl>

<strong>例</strong>:

JSON ファイルからアクセス・グループ・ポリシーを作成します。

```
bluemix iam access-group-policy-create example_group -f @policy.json
```
    
`example_group` に、すべての `sample-service` リソースの `Administrator` 役割を与えます。
```
bluemix iam access-group-policy-create example_group --roles Administrator --service-name sample-service
```

`example_group` に、`us-south` 地域の `sample-service` インスタンス `ServiceId-ade78e9f` のリソース `key123` の `Editor` 役割を与えます。
```
bluemix iam access-group-policy-create example_group --roles Editor --service-name sample-service --service-instance ServiceId-ade78e9f --region us-south --resource-type key --resource key123
```

`example_group` に、リソース・グループ ID `dda27e49d2a1efca58083a01dfde18f6` の `Operator` 役割を与えます。
```
bluemix iam access-group-policy-create example_group --roles Operator --resource-type resource-group --resource dda27e49d2a1efca58083a01dfde18f6
```

`example_group` に、 リソース・グループ `sample-resource-group` のメンバーの `Viewer` 役割を与えます。
```
bluemix iam access-group-policy-create example_group --roles Viewer --resource-group-name sample-resource-group
```

`example_group` に、ID `dda27e49d2a1efca58083a01dfde18f6` を持つリソース・グループのメンバーの `Viewer` 役割を与えます。
```
bluemix iam access-group-policy-create example_group --roles Viewer --resource-group-id dda27e49d2a1efca58083a01dfde18f6
```

## bluemix iam access-group-policy-update
{: #bluemix_iam_access_group_policy_update}

アクセス・グループ・ポリシーを更新します

```
bluemix iam access-group-policy-update GROUP_NAME POLICY_ID [-v, --version VERSION] {-f, --file JSON_FILE | [--roles ROLE_NAME1,ROLE_NAME2...] [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]}
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-f, --file</dt>
  <dd>ポリシー定義の JSON ファイル</dd>
  <dt>-v, --version</dt>
  <dd>ポリシーのバージョン</dd>
  <dt>-roles</dt>
  <dd>ポリシー定義の役割名。 特定のサービスの、サポートされる役割については、「bluemix iam roles --service SERVICE_NAME」を実行してください。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-service-name</dt>
  <dd>ポリシー定義のサービス名。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-service-instance</dt>
  <dd>ポリシー定義のサービス・インスタンス。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-region</dt>
  <dd>ポリシー定義の地域。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-resource-type</dt>
  <dd>ポリシー定義のリソース・タイプ。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-resource</dt>
  <dd>ポリシー定義のリソース。 このオプションは、「-f, --file」と同時に指定することはできません。</dd>
  <dt>-resource-group-name</dt>
  <dd>リソース・グループの名前。 このオプションは、「-f, --file」および「--resource-group-id」と同時に指定することはできません。</dd>
  <dt>-resource-group-id</dt>
  <dd>リソース・グループの ID。 このオプションは、「-f, --file」および「--resource-group-name」と同時に指定することはできません。</dd>
</dl>

<strong>例</strong>:

ポリシー JSON ファイル内のもので、アクセス・グループ・ポリシーを更新します。
```
bluemix iam access-group-policy-update example_group b8638ceb-5c4d-4d58-ae06-7ad95a10c4d4 -f @policy.json
```

`example_group` に、すべての `sample-service` リソースの `Administrator` 役割を与えるようにアクセス・グループ・ポリシーを更新します。
```
bluemix iam access-group-policy-update example_group b8638ceb-5c4d-4d58-ae06-7ad95a10c4d4 --roles Administrator --service-name sample-service
```

`example_group` に、`us-south` 地域の `sample-service` インスタンス `ServiceId-ade78e9f` のリソース `key123` の `Editor` 役割を与えるようにアクセス・グループ・ポリシーを更新します。
```
bluemix iam access-group-policy-update example_group --roles Editor --service-name sample-service --service-instance ServiceId-ade78e9f --region us-south
```

`example_group` に、リソース・グループ ID `dda27e49d2a1efca58083a01dfde18f6` の `Operator` 役割を与えるようにアクセス・グループ・ポリシーを更新します。
```
bluemix iam access-group-policy-update example_group b8638ceb-5c4d-4d58-ae06-7ad95a10c4d4 --roles Operator --resource-type resource-group --resource dda27e49d2a1efca58083a01dfde18f6
```

`example_group` に、リソース・グループ `sample-resource-group` のメンバーの `Viewer` 役割を与えるようにアクセス・グループ・ポリシーを更新します。
```
bluemix iam access-group-policy-update example_group b8638ceb-5c4d-4d58-ae06-7ad95a10c4d4 --roles Viewer --resource-group-name sample-resource-group
```

`example_group` に、ID `dda27e49d2a1efca58083a01dfde18f6` を持つリソース・グループのメンバーの `Viewer` 役割を与えるようにアクセス・グループ・ポリシーを更新します。
```
bluemix iam access-group-policy-update example_group b8638ceb-5c4d-4d58-ae06-7ad95a10c4d4 --roles Viewer --resource-group-id dda27e49d2a1efca58083a01dfde18f6
```

## bluemix iam access-group-policy-delete
{: #bluemix_iam_access_group_policy_delete}

アクセス・グループ・ポリシーを削除します

```
bluemix iam access-group-policy-delete GROUP_NAME POLICY_ID [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>確認なしで削除を強制します</dd>
</dl>

<strong>例</strong>:

アクセス・グループ `example_group` のポリシー `51b9717e-76b0-4f6a-bda7-b8132431f926` を削除します。
```
bluemix iam access-group-policy-delete example_group 51b9717e-76b0-4f6a-bda7-b8132431f926 -f
```

## bluemix iam service-ids
{: #bluemix_iam_service_ids}

すべてのサービス ID をリストします

```
bluemix iam service-ids --uuid
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>--uuid</dt>
  <dd>サービス ID の UUID のみを表示します</dd>
</dl>

<strong>例</strong>:
現行アカウントに含まれているすべてのサービス ID の UUID をリストします

```
bluemix iam service-ids --uuid
```


## bluemix iam service-id
{: #bluemix_iam_service_id}

サービス ID の詳細を表示します

```
bluemix iam service-id (NAME|UUID) [--uuid]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME|UUID (必須)</dt>
  <dd>サービスの名前または UUID</dd>
  <dt>--uuid</dt>
  <dd>サービス ID の UUID を表示します</dd>
</dl>

<strong>例</strong>:

サービス ID `sample-test` の詳細を表示します

```
bluemix iam service-id sample-test
```
サービス ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` の詳細を表示します

```
bluemix iam service-id ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```


## bluemix iam service-id-create
{: #bluemix_iam_service_id_create}

サービス ID を作成します

```
bluemix iam service-id-create NAME [-d, --description DESCRIPTION]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME (必須)</dt>
  <dd>サービスの名前</dd>
  <dt>-d, --description</dt>
  <dd>サービス ID の説明</dd>
</dl>

<strong>例</strong>:

サービス名 `sample-test` と説明 `hello, world!` でサービス ID を作成します

```
bluemix iam service-id-create sample-test -d 'hello, world!'
```


## bluemix iam service-id-update

{: #bluemix_iam_service_id_update}
サービス ID を更新します

```
bluemix iam service-id-update (NAME|UUID) [-n, --name NEW_NAME] [-d, --description DESCRIPTION] [-v, --version VERSION] [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME|UUID (必須)</dt>
  <dd>サービスの名前または UUID</dd>
  <dt>-n, --name</dt>
  <dd>サービスの新しい名前</dd>
  <dt>-d, --description</dt>
  <dd>サービスの新しい説明</dd>
  <dt>-v, --version</dt>
  <dd>サービス ID のバージョン</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに更新します</dd>
</dl>

<strong>例</strong>:

確認を求めずにサービス ID `sample-test` を `sample-test-2` に名前変更します

```
bluemix iam service-id-update sample-test -n sample-test-2 -f
```

サービス `sample-test` バージョン `1-0jn39fbefew` の説明を更新します

```
bluemix iam service-id-update sample-test -d 'hello, friend!' -v 1-0jn39fbefew
```

サービス ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` を `sample-test-3` に名前変更し、説明も新しくします。

```
bluemix iam service-id-update ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 -n sample-test-3 -d 'hello, my friends!' 
```


## bluemix iam service-id-delete
{: #bluemix_iam_service_id_delete}

サービス ID を削除します

```
bluemix iam service-id-delete (NAME|UUID) [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME|UUID (必須)</dt>
  <dd>サービスの名前または UUID</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに削除します</dd>
</dl>

<strong>例</strong>:

確認を求めずにサービス ID `sample-teset` を削除します

```
bluemix iam service-id-delete sample-teset -f
```

サービス ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` を削除します

```
bluemix iam service-id-delete ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```


## bluemix iam api-keys
{: #bluemix_iam_api_keys}

すべての {{site.data.keyword.Bluemix_notm}} プラットフォーム API キーをリストします

```
bluemix iam api-keys
```

<strong>前提条件</strong>: エンドポイント、ログイン

## bluemix iam api-key-create
{: #bluemix_iam_api_key_create}

新しい {{site.data.keyword.Bluemix_notm}} プラットフォーム API キーを作成します

```
bluemix iam api-key-create NAME [-d DESCRIPTION] [--file FILE]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
<dt>NAME (必須)</dt>
<dd>作成する API キーの名前。</dd>
<dt>-d <i>DESCRIPTION</i> (オプション)</dt>
<dd>API キーの説明</dd>
<dt>--file <i>FILE</i></dt>
<dd>指定されたファイルに API キー情報を保存します。 設定されていない場合、JSON コンテンツが表示されます。</dd>
</dl>

<strong>例</strong>:

API キーを作成し、ファイルに保存します

```
bluemix iam api-key-create MyKey -d "this is my API key" --file key_file
```

## bluemix iam api-key-update
{: #bluemix_iam_api_key_update}

{{site.data.keyword.Bluemix_notm}} プラットフォーム API キーを更新します

```
bluemix iam api-key-update NAME [-n NAME] [-d DESCRIPTION]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
<dt>NAME (必須)</dt>
<dd>更新する API キーの古い名前。</dd>
<dt>-n <i>NAME</i> (オプション)</dt>
<dd>API キーの新しい名前</dd>
<dt>-d <i>DESCRIPTION</i> (オプション)</dt>
<dd>API キーの新しい説明</dd>
</dl>

<strong>例</strong>:

API キーの説明を更新します。

```
bluemix iam api-key-update MyKey -d "the new description of my key"
```

## bluemix api-key-delete
{: #bluemix_api_key_delete}

{{site.data.keyword.Bluemix_notm}} プラットフォーム API キーを削除します

```
bluemix iam api-key-delete NAME [-f]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
<dt>NAME (必須)</dt>
<dd>削除する API キーの名前。</dd>
<dt>-f (オプション)</dt>
<dd>確認なしで削除を強制します。</dd>
</dl>

## bluemix iam service-api-keys
{: #bluemix_iam_service_api_keys}

サービスのすべての API キーをリストします

```
bluemix iam service-api-keys SERVICE_ID [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずにサービス API キーを表示します</dd>
</dl>

<strong>例</strong>:

サービス `sample-service` のすべての API キーをリストします

```
bluemix iam service-api-keys sample-service
```

## bluemix iam service-api-key
{: #bluemix_iam_service_api_key}

サービス API キーの詳細をリストします

```
bluemix iam service-api-key NAME SERVICE_ID [--uuid] [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>--uuid</dt>
  <dd>サービス API キーの UUID を表示します</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずにサービス API キーを表示します</dd>
</dl>

<strong>例</strong>:

サービス `sample-service` のサービス API キー `sample-key` の詳細を表示します

```
bluemix iam service-api-key sample-key sample-service
```

## bluemix iam service-api-key-create
{: #bluemix_iam_service_api_key_create}

サービス API キーを作成します

```
bluemix iam service-api-key-create NAME SERVICE_ID [-d, --description DESCRIPTION] [--file FILE] [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>-d, --description</dt>
  <dd>API キーの説明</dd>
  <dt>--file</dt>
  <dd>指定されたファイルに API キー情報を保存します。 設定されていない場合、JSON コンテンツが表示されます。</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに作成を強制します</dd>
</dl>

<strong>例</strong>:

確認を求めずにサービス `sample-service` のサービス API キー `sample-key` を作成します。

```
bluemix iam service-api-key-create sample-key sample-service -f
```

## bluemix iam service-api-key-update
{: #bluemix_iam_service_api_key_update}

サービス API キーを更新します

```
bluemix iam service-api-key-update NAME SERVICE_ID  [-n, --name NEW_sNAME] [-d, --description DESCRIPTION] [-v, --version VERSION] [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>-n, --name</dt>
  <dd>サービスAPI キーの新しい名前</dd>
  <dt>-d, --description</dt>
  <dd>サービス API キーの新しい説明</dd>
  <dt>-v, --version</dt>
  <dd>サービス API キーのバージョン</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに更新します</dd>
</dl>

<strong>例</strong>:

サービス API キー `sample-key` を `new-sample-key` に名前変更します

```
bluemix iam service-api-key-update sample-key sample-service -n new-sample-key
```

## bluemix iam service-api-key-delete
{: #bluemix_iam_service_api_key_delete}

サービス API キーを削除します

```
bluemix iam service-api-key-delete NAME SERVICE_ID [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに削除します</dd>
</dl>

<strong>例</strong>:

サービス API キー `sample-key` を削除します

```
bluemix iam service-api-key-delete sample-key sample-service
```

## bluemix iam user-policies
{: #bluemix_iam_user_policies}

ユーザー `name@example.com` のポリシーをリストします

```
bluemix iam user-policies name@example.com
```

<strong>前提条件</strong>:  エンドポイント、ログイン、ターゲットのアカウント

<strong>コマンド・オプション</strong>:
<dl>
<dt>USER_NAME (必須)</dt>
<dd>ポリシーが属するユーザー名</dd>
</dl>

<strong>例</strong>:

ユーザー `name@example.com` のポリシーをリストします

```
bluemix iam user-policies name@example.com
```

## bluemix iam user-policy
{: #bluemix_iam_user_policy}

ユーザー・ポリシーの詳細を表示します

```
bluemix iam user-policy USER_NAME POLICY_ID
```

<strong>前提条件</strong>:  エンドポイント、ログイン、ターゲットのアカウント

<strong>コマンド・オプション</strong>:
<dl>
<dt>USER_NAME (必須)</dt>
<dd>ポリシーが属するユーザー名</dd>
<dt>POLICY_ID (必須)</dt>
<dd>ポリシーの ID</dd>
</dl>

<strong>例</strong>:

ユーザー `name@example.com` のポリシー `0bb730daa` をリストします

```
bluemix iam user-policy name@example.com 0bb730daa
```

## bluemix iam user-policy-create
{: #bluemix_iam_user_policy_create}

ユーザー・ポリシーを作成します

```
bluemix iam user-policy-create USER_NAME {--file JSON_FILE | --roles ROLE_NAME1,ROLE_NAME2... [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]}
```

<strong>前提条件</strong>:  エンドポイント、ログイン、ターゲットのアカウント

<strong>コマンド・オプション</strong>:
<dl>
<dt>USER_NAME (必須)</dt>
<dd>ポリシーが属するユーザー名</dd>
<dt>--file <i>FILE</i> (オプション)</dt>
<dd>ポリシー定義の JSON ファイル</dd>
<dt>--roles <i>ROLE_NAME1,ROLE_NAME2...</i> (オプション)</dt>
<dd>ポリシー定義の役割名。 特定のサービスの、サポートされる役割については、「bluemix iam roles --service SERVICE_NAME」を実行してください。 このオプションは、「--file」と同時に指定することはできません。</dd>
<dt>--service-name <i>SERVICE_NAME</i> (オプション)</dt>
<dd>ポリシー定義のサービス名。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--serivce-instance <i>SERVICE_INSTANCE</i> (オプション)</dt>
<dd>ポリシー定義のサービス・インスタンス。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--region <i>REGION</i> (オプション)</dt>
<dd>ポリシー定義の地域。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--resource-type <i>RESOURCE_TYPE</i> (オプション)</dt>
<dd>ポリシー定義のリソース・タイプ。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--resource <i>RESOURCE</i> (オプション)</dt>
<dd>ポリシー定義のリソース。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--resource-group-name <i>RESOURCE_GROUP_NAME</i> (オプション)</dt>
<dd>リソース・グループの名前。これは、「--file」、「--resource」、および「--resource-group-id」の各フラグと同時に指定することはできません。</dd>
<dt>--resource-group-id <i>RESOURCE_GROUP_ID</i> (オプション)</dt>
<dd>リソース・グループの ID。これは、「--file」、「--resource」、および「--resource-group-id」の各フラグと同時に指定することはできません。</dd>
</dl>

<strong>例</strong>:

ポリシー JSON ファイル `policy.json` から、ユーザー `name@example.com` のユーザー・ポリシーを作成します。

```
bluemix iam user-policy-create name@example.com --file @policy.json
```

`name@example.com` に、すべての `sample-service` リソースの `Administrator` 役割を与えます。

```
bluemix iam user-policy-create name@example.com --roles Administrator --service-name sample-service
```

`name@example.com` に、`us-south` 地域のサンプル・サービス・インスタンス `ServiceId-ade78e9f` のリソース `key123` の `Editor` 役割を与えます。

```
bluemix iam user-policy-create name@example.com --roles Editor --service-name sample-service --service-instance ServiceId-ade78e9f --region us-south --resource-type key --resource key123
```

`name@example.com` に、リソース・グループ ID `dda27e49d2a1efca58083a01dfde18f6` の `Operator` 役割を与えます。

```
bluemix iam user-policy-create name@example.com --roles Operator --resource-type resource-group --resource dda27e49d2a1efca58083a01dfde18f6
```

`name@example.com` に、 リソース・グループ `sample-resource-group` のメンバーの `Viewer` 役割を与えます。

```
bluemix iam user-policy-create name@example.com --roles Viewer --resource-group-name sample-resource-group
```

`name@example.com` に、ID `dda27e49d2a1efca58083a01dfde18f6` を持つリソース・グループのメンバーの `Viewer` 役割を与えます。

```
bluemix iam user-policy-create name@example.com --roles Viewer --resource-group-id dda27e49d2a1efca58083a01dfde18f6
```

## bluemix iam user-policy-update
{: #bluemix_iam_user_policy_update}

ユーザー・ポリシーを更新します

```
bluemix iam user-policy-update USER_NAME POLICY_ID [-v, --version VERSION] {--file JSON_FILE | [--roles ROLE_NAME1,ROLE_NAME2...] [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]}
```

<strong>前提条件</strong>:  エンドポイント、ログイン、ターゲットのアカウント

<strong>コマンド・オプション</strong>:
<dt>USER_NAME (必須)</dt>
<dd>ポリシーが属するユーザー名</dd>
<dt>POLICY_ID (必須)</dt>
<dd>更新するポリシーの ID</dd>
<dt>-v, --version <i>VERSION</i> (オプション)</dt>
<dd>既存のポリシーのバージョン</dd>
<dt>--file <i>FILE</i> (オプション)</dt>
<dd>ポリシー定義の JSON ファイル</dd>
<dt>--roles <i>ROLE_NAME1,ROLE_NAME2...</i> (オプション)</dt>
<dd>ポリシー定義の役割名。 特定のサービスの、サポートされる役割については、「bluemix iam roles --service SERVICE_NAME」を実行してください。 このオプションは、「--file」と同時に指定することはできません。</dd>
<dt>--service-name <i>SERVICE_NAME</i> (オプション)</dt>
<dd>ポリシー定義のサービス名。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--serivce-instance <i>SERVICE_INSTANCE</i> (オプション)</dt>
<dd>ポリシー定義のサービス・インスタンス。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--region <i>REGION</i> (オプション)</dt>
<dd>ポリシー定義の地域。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--resource-type <i>RESOURCE_TYPE</i> (オプション)</dt>
<dd>ポリシー定義のリソース・タイプ。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--resource <i>RESOURCE</i> (オプション)</dt>
<dd>ポリシー定義のリソース。これは、「--file」フラグと同時に指定することはできません。</dd>
<dt>--resource-group-name <i>RESOURCE_GROUP_NAME</i> (オプション)</dt>
<dd>リソース・グループの名前。これは、「--file」、「--resource」、および「--resource-group-id」の各フラグと同時に指定することはできません。</dd>
<dt>--resource-group-id <i>RESOURCE_GROUP_ID</i> (オプション)</dt>
<dd>リソース・グループの ID。これは、「--file」、「--resource」、および「--resource-group-id」の各フラグと同時に指定することはできません。</dd>
</dl>

<strong>例</strong>:

JSON ファイル内のポリシーによってユーザー・ポリシーを更新します

```
bluemix iam user-policy-update name@example.com 0bb730daa --file @policy.json
```

`name@example.com` に、すべての `sample-service` リソースの `Administrator` 役割を与えるようにユーザー・ポリシーを更新します

```
bluemix iam user-policy-update name@example.com user-policy-id --roles Administrator --service-name sample-service
```

 `name@example.com` に、`us-south` 地域のサンプル・サービス・インスタンス `ServiceId-ade78e9f` のリソース `key123` の `Editor` 役割を与えるようにユーザー・ポリシーを更新します

```
bluemix iam user-policy-update name@example.com --roles Editor --service-name sample-service --service-instance ServiceId-ade78e9f --region us-south --resource-type key --resource key123
```

`name@example.com` に、リソース・グループ ID `dda27e49d2a1efca58083a01dfde18f6` の `Operator` 役割を与えるようにユーザー・ポリシーを更新します

```
bluemix iam user-policy-update name@example.com user-policy-id --roles Operator --resource-type resource-group --resource dda27e49d2a1efca58083a01dfde18f6
```

`name@example.com` に、 リソース・グループ `sample-resource-group` のメンバーの `Viewer` 役割を与えるようにユーザー・ポリシーを更新します

```
bluemix iam user-policy-update name@example.com user-policy-id --roles Viewer --resource-group-name sample-resource-group
```

`name@example.com` に、ID `dda27e49d2a1efca58083a01dfde18f6` を持つリソース・グループのメンバーの `Viewer` 役割を与えるようにユーザー・ポリシーを更新します

```
bluemix iam user-policy-update name@example.com user-policy-id --roles Viewer --resource-group-id dda27e49d2a1efca58083a01dfde18f6
```



## bluemix iam service-policies
{: #bluemix_iam_service_policies}

指定したサービスのすべてのサービス・ポリシーをリストします

```
bluemix iam service-policies SERVICE_ID [--json] [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>-json</dt>
  <dd>JSON フォーマットでポリシーを表示します</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずにサービス・ポリシーを表示します</dd>
</dl>

<strong>例</strong>:

サービス `test` のポリシーをリストします

```
bluemix iam service-policies test
```
サービス `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` のポリシーをリストします

```
bluemix iam service-policies ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```


## bluemix iam service-policy
{: #bluemix_iam_service_policy}

サービス・ポリシーの詳細を表示します

```
bluemix iam service-policy SERVICE_ID POLICY_ID [--json] [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>POLICY_ID (必須)</dt>
  <dd>サービス・ポリシーの ID<dd>
  <dt>-json</dt>
  <dd>JSON フォーマットでポリシーを表示します</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずにサービス・ポリシーを表示します</dd>
</dl>

<strong>例</strong>:

サービス `test` のポリシー `140798e2-8ea7db3` を表示します

```
bluemix iam service-policies test 140798e2-8ea7db3
```
サービス `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` のポリシー `140798e2-8ea7db3` を表示します

```
bluemix iam service-policies ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 140798e2-8ea7db3
```


## bluemix iam service-policy-create
{: #bluemix_iam_service_policy_create}

サービス・ポリシーを作成します

```
bluemix iam service-policy-create SERVICE_ID {--file JSON_FILE | -r, --roles ROLE_NAME1,ROLE_NAME2... [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]} [-f, --force]",
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>--file</dt>
  <dd>ポリシー定義の JSON ファイル。 これは、「-r, --roles」、「--service-name」、「--service-instance」、「--region」、「--resource-type」、「--resource」、「--resource-group-name」、および「--resource-group-id」の各フラグと同時に指定することはできません。</dd>
  <dt>-r, --roles</dt>
  <dd>ポリシー定義の役割名。 特定のサービスの、サポートされる役割については、「bluemix iam roles --service SERVICE_NAME」を実行してください。 このオプションは、「--file」と同時に指定することはできません。</dd>
  <dt>--service-name</dt>
  <dd>ポリシー定義のサービス名。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>--service-instance</dt>
  <dd>ポリシー定義のサービス・インスタンス。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>-region</dt>
  <dd>ポリシー定義の地域。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>--resource-type</dt>
  <dd>ポリシー定義のリソース・タイプ。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>--resource</dt>
  <dd>ポリシー定義のリソース。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>--resource-group-name</dt>
  <dd>リソース・グループの名前。 このオプションは、「--file」および「--resource-group-id」と同時に指定することはできません。</dd>
  <dt>--resource-group-id </dt>
  <dd>リソース・グループの ID。 このオプションは、「--file」および「--resource-group-name」と同時に指定することはできません。</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずにサービス・ポリシーを作成します</dd>
</dl>

<strong>例</strong>:

サービス `test` のサービス・ポリシーを JSON ファイルから作成します

```
bluemix iam service-policy-create test --file @policy.json
```
サービス `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` のサービス・ポリシーを JSON ファイルから作成します

```
bluemix iam service-policy-create ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 --file @policy.json
```


## bluemix iam service-policy-update
{: #bluemix_iam_service_policy_update}

サービス・ポリシーを更新します

```
bluemix iam service-policy-update SERVICE_ID POLICY_ID [-v, --version VERSION] {--file JSON_FILE | [-r, --roles ROLE_NAME1,ROLE_NAME2...] [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]} [-f, --force]",
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>POLICY_ID (必須)</dt>
  <dd>サービス・ポリシーの ID<dd>
  <dt>-v, --version</dt>
  <dd>サービス・ポリシーのバージョン</dd>
  <dt>--file</dt>
  <dd>ポリシー定義の JSON ファイル。 これは、「-r, --roles」、「--service-name」、「--service-instance」、「--region」、「--resource-type」、「--resource」、「--resource-group-name」、および「--resource-group-id」の各フラグと同時に指定することはできません。</dd>
  <dt>-r, --roles</dt>
  <dd>ポリシー定義の役割名。 特定のサービスの、サポートされる役割については、「bluemix iam roles --service SERVICE_NAME」を実行してください。 このオプションは、「--file」と同時に指定することはできません。</dd>
  <dt>-service-name</dt>
  <dd>ポリシー定義のサービス名。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>-service-instance</dt>
  <dd>ポリシー定義のサービス・インスタンス。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>-region</dt>
  <dd>ポリシー定義の地域。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>-resource-type</dt>
  <dd>ポリシー定義のリソース・タイプ。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>-resource</dt>
  <dd>ポリシー定義のリソース。 これは、「--file」フラグと同時に指定することはできません。</dd>
  <dt>--resource-group-name</dt>
  <dd>リソース・グループの名前。 このオプションは、「--file」および「--resource-group-id」と同時に指定することはできません。</dd>
  <dt>--resource-group-id </dt>
  <dd>リソース・グループの ID。 このオプションは、「--file」および「--resource-group-name」と同時に指定することはできません。</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずにサービス・ポリシーを更新します</dd>
</dl>

<strong>例</strong>:

サービス `test` のサービス・ポリシー `140798e2-8ea7db3` を JSON ファイルから更新します

```
bluemix iam service-policy-update test 140798e2-8ea7db3 --file @policy.json
```
サービス `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` のサービス・ポリシー `140798e2-8ea7db3` を JSON ファイルから更新します

```
bluemix iam service-policy-update ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 140798e2-8ea7db3 --file @policy.json
```

## bluemix iam service-policy-delete
{: #bluemix_iam_service_policy_delete}

サービス・ポリシーを削除します

```
bluemix iam service-policy-delete SERVICE_ID POLICY_ID [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ID (必須)</dt>
  <dd>サービス ID の名前または UUID</dd>
  <dt>POLICY_ID (必須)</dt>
  <dd>サービス・ポリシーの ID<dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに削除します</dd>
</dl>

<strong>例</strong>:

サービス `test` のポリシー `140798e2-8ea7db3` を削除します

```
bluemix iam service-policy-delete test 140798e2-8ea7db3
```
サービス `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976` のポリシー `140798e2-8ea7db3` を削除します

```
bluemix iam service-policy-delete ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976 140798e2-8ea7db3
```

## bluemix iam oauth-tokens
{: #bluemix_iam_oauth_tokens}

現行セッションの OAuth トークンを取得して表示します

```
bluemix iam oauth-tokens
```

<strong>前提条件</strong>: ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

OAuth トークンを更新して表示します

```
bluemix iam oauth-tokens
```

## bluemix iam dedicated-id-disconnect
{: #bluemix_iam_dedicated_id_disconnect}

パブリック IBM ID を専用の非 IBM ID から切断します

```
bluemix iam dedicated-id-disconnect [-f, --force]
```

<strong>前提条件</strong>: ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>確認なしで切断を強制します</dd>
</dl>


## bluemix iam authorization-policy-create
{: #bluemix_iam_authorization_policy_create}

特定のサービス・インスタンスが別のサービス・インスタンスへアクセスできるようにするための許可ポリシーを作成します。

```
bluemix iam authorization-policy-create SOURCE_SERVICE_NAME TARGET_SERVICE_NAME [—-source-service-instance SOURCE_SERVICE_INSTANCE_NAME] [—-target-service-instance TARGET_SERVICE_INSTANCE_NAME] ROLE_NAME1,ROLE_NAME2...
```

<strong>前提条件</strong>: ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SOURCE_SERVICE_NAME</dt>
  <dd>アクセスを許可されるソース・サービス。</dd>
  <dt>TARGET_SERVICE_NAME</dt>
  <dd>ソース・サービスがアクセスを許可されるターゲット・サービス。</dd>
  <dt>—-source-service-instance SOURCE_SERVICE_INSTANCE_NAME</dt>
  <dd>ソース・サービスのインスタンス名。指定されない場合、ソース・サービスのすべてのインスタンスがアクセスを許可されます。</dd>
  <dt>—-target-service-instance TARGET_SERVICE_INSTANCE_NAME</dt>
  <dd>ターゲット・サービスのインスタンス名。指定されない場合、ターゲット・サービスのすべてのインスタンスがアクセスを許可されます。</dd>
  <dt>ROLE_NAME1,ROLE_NAME2...</dt>
  <dd>ソース・サービスのアクセス権限を提供する役割。</dd>  
</dl>

## bluemix iam authorization-policy-delete
{: #bluemix_iam_authorization_policy_delete}

許可ポリシーを削除します。

```
bluemix iam authorization-policy-delete AUTHORIZATION_POLICY_ID [-f, --force]
```

<strong>前提条件</strong>: ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>AUTHORIZATION_POLICY_ID</dt>
  <dd>削除する許可ポリシーの ID。</dd> 
  <dt>-f, --force</dt>
  <dd>確認なしで削除を強制します。</dd> 
</dl>

## bluemix iam authorization-policy
{: #bluemix_iam_authorization_policy}

許可ポリシーの詳細を表示します。

```
bluemix iam authorization-policy AUTHORIZATION_POLICY_ID
```

<strong>前提条件</strong>: ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>AUTHORIZATION_POLICY_ID</dt>
  <dd>表示する許可ポリシーの ID。</dd> 
</dl>


## bluemix iam authorization-policies
{: #bluemix_iam_authorization_policies}

現行アカウントの許可ポリシーをリストします。

```
bluemix iam authorization-policies
```

<strong>前提条件</strong>: ログイン、ターゲット


## bluemix resource groups
{: #bluemix_resource_groups}

リソース・グループをリストします。

```
bluemix resource groups [--default]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>--default</dt>
  <dd>現行アカウントのデフォルト・グループを取得します。</dd>
</dl>

<strong>例</strong>:

現在のターゲット・アカウントのすべてのリソース・グループをリストします

```
bluemix resource groups
```

現在のターゲット・アカウントのデフォルト・グループをリストします

```
bluemix resource groups --default
```

## bluemix resource group
{: #bluemix_resource_group}

リソース・グループの詳細を表示します

```
bluemix resource group NAME [--id]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME (必須)</dt>
  <dd>リソース・グループの名前</dd>
  <dt>--id</dt>
  <dd>ID のみを表示します</dd>
</dl>

<strong>例</strong>:

リソース・グループ `example-group` を表示します

```
bluemix resource group example-group
```

リソース・グループ `example-group` の ID のみを表示します

```
bluemix resource group example-group --id
```


## bluemix resource group-update
{: #bluemix_resource_group_update}

既存のリソース・グループを更新します

```
bluemix resource group-update NAME [-n, --name NEW_NAME] [-q, --quota NEW_QUOTA_NAME]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME (必須)</dt>
  <dd>ターゲット・リソース・グループの名前</dd>
  <dt>-n, --name</dt>
  <dd>リソース・グループの新しい名前</dd>
  <dt>-q, --quota</dt>
  <dd>新規割り当て量定義の名前</dd>
  <dt>-f</dt>
  <dd>確認を求めずに更新を強制します</dd>
</dl>

<strong>例</strong>:

リソース・グループ `example-group` を `trial-group` に名前変更します

```
bluemix resource group-update example-group -n trial-group
```

リソース・グループ `example-group` の割り当て量を `free` に変更します

```
bluemix resource group-update example-group -q free
```

## bluemix resource quotas
{: #bluemix_resource_quotas}

すべての割り当て量定義をリストします

```
bluemix resource quotas
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
</dl>

<strong>例</strong>:

すべての割り当て量定義をリストします

```
bluemix resource quotas
```

## bluemix resource quota
{: #bluemix_resource_quota}

割り当て量定義の詳細を表示します

```
bluemix resource quota NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME (必須)</dt>
  <dd>割り当て量の名前</dd>
</dl>

<strong>例</strong>:
割り当て量 `free` の詳細を表示します

```
bluemix resource quota free
```


## bluemix app push
{: #bluemix_app_push}

このコマンドの機能とオプションは [cf push![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/push.html){: new_window} コマンドと同じです。


## bluemix app list
{: #bluemix_app_list}

このコマンドの機能とオプションは [cf apps![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/apps.html){: new_window} コマンドと同じです。


## bluemix app show
{: #bluemix_app_show}

このコマンドの機能とオプションは [cf app![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/app.html){: new_window} コマンドと同じです。


## bluemix app delete
{: #bluemix_app_delete}

このコマンドの機能とオプションは [cf delete![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/delete.html){: new_window} コマンドと同じです。


## bluemix app rename
{: #bluemix_app_rename}

このコマンドの機能とオプションは [cf rename![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/rename.html){: new_window} コマンドと同じです。


## bluemix app start
{: #bluemix_app_start}

このコマンドの機能とオプションは [cf start![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/start.html){: new_window} コマンドと同じです。


## bluemix app stop
{: #bluemix_app_stop}

このコマンドの機能とオプションは [cf stop![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/stop.html){: new_window} コマンドと同じです。


## bluemix app restart
{: #bluemix_app_restart}

このコマンドの機能とオプションは [cf restart![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/restart.html){: new_window} コマンドと同じです。


## bluemix app restage
{: #bluemix_app_restage}


このコマンドの機能とオプションは [cf restage![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/restage.html){: new_window} コマンドと同じです。


## bluemix app instance-restart
{: #bluemix_app_instance_restart}


このコマンドの機能とオプションは [cf restart-app-instance![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/restart-app-instance.html){: new_window} コマンドと同じです。


## bluemix app events
{: #bluemix_app_events}

このコマンドの機能とオプションは [cf events![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/events.html){: new_window} コマンドと同じです。


## bluemix app files
{: #bluemix_app_files}

このコマンドの機能とオプションは [cf files![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/files.html){: new_window} コマンドと同じです。


## bluemix app logs
{: #bluemix_app_logs}

このコマンドの機能とオプションは [cf logs![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/logs.html){: new_window} コマンドと同じです。


## bluemix app env
{: #bluemix_app_env}

このコマンドの機能とオプションは [cf env![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/env.html){: new_window} コマンドと同じです。


## bluemix app env-set
{: #bluemix_app_env_set}

このコマンドの機能とオプションは [cf set-env![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/set-env.html){: new_window} コマンドと同じです。


## bluemix app env-unset
{: #bluemix_app_env_unset}

このコマンドの機能とオプションは [cf unset-env![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/unset-env.html){: new_window} コマンドと同じです。


## bluemix app stacks
{: #bluemix_app_stacks}

このコマンドの機能とオプションは [cf stacks![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/stacks.html){: new_window} コマンドと同じです。


## bluemix app stack-show
{: #bluemix_app_stack_show}

このコマンドの機能とオプションは [cf stack![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/stack.html){: new_window} コマンドと同じです。


## bluemix app manifest-create
{: #bluemix_app_manifest_create}

このコマンドの機能とオプションは [cf create-app-manifest![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/create-app-manifest.html){: new_window} コマンドと同じです。

## bluemix app domain-cert
{: #bluemix_app_domain_cert}

ドメインの証明書情報をリストします。

```
bluemix app domain-cert DOMAIN_NAME
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
<dt>DOMAIN_NAME (必須)</dt>
<dd>証明書をホストするドメイン。</dd>
</dl>


<strong>例</strong>:

ドメイン `ibmcxo-eventconnect.com` の証明書情報を表示するには、次のように指定します。

```
bluemix app domain-cert ibmcxo-eventconnect.com
```

## bluemix app domain-cert-add
{: #bluemix_app_domain_cert_add}

現在の組織内の、指定したドメインに証明書を追加します。

```
bluemix app domain-cert-add DOMAIN -k PRIVATE_KEY_FILE -c CERT_FILE [-p PASSWORD] [-i INTERMEDIATE_CERT_FILE] [-t TRUST_STORE_FILE]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>DOMAIN (必須)</dt>
   <dd>証明書を追加するドメイン。</dd>
   <dt>-k <i>PRIVATE_KEY_FILE</i> (必須)</dt>
   <dd>秘密鍵ファイル・パス。</dd>
   <dt>-c <i>CERT_FILE</i> (必須)</dt>
   <dd>証明書ファイル・パス。</dd>
   <dt>-p <i>PASSWORD</i> (オプション)</dt>
   <dd>証明書のパスワード。</dd>
   <dt>-i <i>INTERMEDIATE_CERT_FILE</i> (オプション)</dt>
   <dd>中間証明書ファイル・パス。</dd>
   <dt>-t <i>TRUST_STORE_FILE</i> (オプション)</dt>
   <dd>トラストストア・ファイル。</dd>
   </dl>


<strong>例</strong>:

ドメイン `ibmcxo-eventconnect.com` に証明書を追加するには、以下のように指定します。

```
bluemix app domain-cert-add ibmcxo-eventconnect.com -k key_file.key -c cert_file.crt -p 123 -i inter_cert.cert
```

## bluemix app domain-cert-remove
{: #bluemix_app_domain_cert_remove}

現在の組織内の、指定したドメインから証明書を削除します。

```
bluemix app domain-cert-remove DOMAIN [-f]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>DOMAIN (必須)</dt>
   <dd>証明書を削除するドメイン。</dd>
   <dt>-f (オプション)</dt>
   <dd>確認なしで削除を強制します。</dd>
   </dl>

## bluemix app routes
{: #bluemix_app_routes}

このコマンドの機能とオプションは [cf routes![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/routes.html){: new_window} コマンドと同じです。


## bluemix app route-check
{: #bluemix_app_route_check}

このコマンドの機能とオプションは [cf check-route![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/check-route.html){: new_window} コマンドと同じです。


## bluemix app route-map
{: #bluemix_app_route_map}

指定されたドメインおよびホスト名を持つ経路を既存 cf アプリケーションまたはコンテナー・グループにマップします。

```
bluemix app route-map CF_APP_NAME|CONTAINER_GROUP_NAME  DOMAIN  [-n HOST_NAME]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>CF_APP_NAME|CONTAINER_GROUP_NAME (必須)</dt>
   <dd>経路によってマップされる cf アプリケーションまたはコンテナー・
グループの名前。</dd>
   <dt>DOMAIN (必須)</dt>
   <dd>経路のドメイン。 例えば、mychinabluemix.net または chinabluemix.net などです。 </dd>
   <dt>-n <i>HOST_NAME</i> (オプション)</dt>
   <dd>経路のホスト名。 指定されない場合、ホスト名は、デフォルトで、アプリケーション名またはコンテナー・グループ名に設定されます。</dd>
   </dl>

<strong>例</strong>:

指定されたドメインで `my-app` に経路をマップします。

```
bluemix app route-map my-app mychinabluemix.net
```

指定されたドメインとホスト名で「my-container-group」に経路をマップします。

```
bluemix app route-map my-container-group chinabluemix.net -n abc
```


## bluemix app route-unmap
{: #bluemix_app_route_unmap}

指定された経路を既存 cf アプリケーションまたはコンテナー・グループからマップ解除します。

```
bluemix app route-unmap CF_APP_NAME|CONTAINER_GROUP_NAME  DOMAIN  [-n HOST_NAME]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>CF_APP_NAME|CONTAINER_GROUP_NAME (必須)</dt>
   <dd>cf アプリケーションまたはコンテナー・グループの名前。</dd>
   <dt>DOMAIN (必須)</dt>
   <dd>経路のドメイン (例えば、mychinabluemix.net または chinabluemix.net)。</dd>
   <dt>-n <i>HOST_NAME</i> (オプション)</dt>
   <dd>経路のホスト名。 指定されない場合、ホスト名は、デフォルトで、アプリケーション名またはコンテナー・グループ名に設定されます。</dd>
   </dl>

<strong>例</strong>:

`my-app.mychinabluemix.net` を `my-app` からマップ解除するには、以下のように指定します。

```
bluemix app route-unmap my-app mychianbluemix.net
```

`abc.chinabluexmix.net` を `my-container-group` からマップ解除するには、以下のように指定します。

```
bluemix app route-unmap my-container-group chinabluemix.net -n abc
```


## bluemix app route-create
{: #bluemix_app_route_create}

このコマンドの機能とオプションは [cf create-route![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/create-route.html){: new_window} コマンドと同じです。


## bluemix app route-delete
{: #bluemix_app_route_delete}

このコマンドの機能とオプションは [cf delete-route![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/delete-route.html){: new_window} コマンドと同じです。


## bluemix app orphaned-routes-delete
{: #bluemix_app_orphaned_routes_delete}

このコマンドの機能とオプションは [cf delete-orphaned-routes![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/delete-orphaned-routes.html){: new_window} コマンドと同じです。


## bluemix app domains
{: #bluemix_app_domains}

このコマンドの機能とオプションは [cf domains![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/domains.html){: new_window} コマンドと同じです。


## bluemix app domain-create
{: #bluemix_app_domain_create}

このコマンドの機能とオプションは [cf create-domain![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/create-domain.html){: new_window} コマンドと同じです。


## bluemix app domain-delete
{: #bluemix_app_domain_delete}

このコマンドの機能とオプションは [cf delete-domain![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/delete-domain.html){: new_window} コマンドと同じです。


## bluemix app shared-domain-create
{: #bluemix_app_shared_domain_create}

このコマンドの機能とオプションは [cf create-shared-domain![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/create-shared-domain.html){: new_window} コマンドと同じです。


## bluemix app shared-domain-delete
{: #bluemix_app_shared_domain_delete}

このコマンドの機能とオプションは [cf delete-shared-domain![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/delete-shared-domain.html){: new_window} コマンドと同じです。


## bluemix service offerings
{: #bluemix_service_offerings}


このコマンドの機能とオプションは [cf marketplace![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/marketplace.html){: new_window} コマンドと同じです。


## bluemix service list
{: #bluemix_service_list}

このコマンドの機能とオプションは [cf services![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/services.html){: new_window} コマンドと同じです。


## bluemix service show
{: #bluemix_service_show}

このコマンドの機能とオプションは [cf service![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/service.html){: new_window} コマンドと同じです。


## bluemix service create
{: #bluemix_service_create}

このコマンドの機能とオプションは [cf create-service![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/create-service.html){: new_window} コマンドと同じです。


## bluemix service update
{: #bluemix_service_update}

このコマンドの機能とオプションは [cf update-service![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/update-service.html){: new_window} コマンドと同じです。


## bluemix service delete
{: #bluemix_service_delete}

このコマンドの機能とオプションは [cf delete-service![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/delete-service.html){: new_window} コマンドと同じです。


## bluemix service rename
{: #bluemix_service_rename}

このコマンドの機能とオプションは [cf rename-service![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/rename-service.html){: new_window} コマンドと同じです。


## bluemix service bind
{: #bluemix_service_bind}

このコマンドの機能とオプションは [cf bind-service![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/bind-service.html){: new_window} コマンドと同じです。


## bluemix service unbind
{: #bluemix_service_unbind}

このコマンドの機能とオプションは [cf unbind-service![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/unbind-service.html){: new_window} コマンドと同じです。


## bluemix service key-create
{: #bluemix_service_key_create}

このコマンドの機能とオプションは [cf create-service-key![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/create-service-key.html){: new_window} コマンドと同じです。


## bluemix service key-delete
{: #bluemix_service_key_delete}

このコマンドの機能とオプションは [cf delete-service-key![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/delete-service-key.html){: new_window} コマンドと同じです。


## bluemix service keys
{: #bluemix_service_keys}

このコマンドの機能とオプションは [cf service-keys![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/service-keys.html){: new_window} コマンドと同じです。


## bluemix service key-show
{: #bluemix_service_key_show}

このコマンドの機能とオプションは [cf service-key![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/service-key.html){: new_window} コマンドと同じです。


## bluemix service user-provided-create
{: #bluemix_service_user_provided_create}

このコマンドの機能とオプションは [cf create-user-provided-service![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/create-user-provided-service.html){: new_window} コマンドと同じです。


## bluemix service user-provided-update
{: #bluemix_service_user_provided_update}

このコマンドの機能とオプションは [cf update-user-provided-service![外部リンク・アイコン](../../../icons/launch-glyph.svg)](http://cli.cloudfoundry.org/en-US/cf/update-user-provided-service.html){: new_window} コマンドと同じです。


## bluemix resource service-instances
{: #bluemix_resource_service_instances}

サービス・インスタンスをリストします

```
bluemix resource service-instances [--service-name SERVICE_NAME] [--location LOCATION] [--long]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>--service-name</dt>
  <dd>従属サービスの名前</dd>
  <dt>--location</dt>
  <dd>場所を基準にフィルター操作します</dd>
  <dt>--long</dt>
  <dd>出力に追加フィールドを表示します</dd>
</dl>

<strong>例</strong>:

サービス `test-service` のサービス・インスタンスをリストします。

```
bluemix resource service-instances --service-name test-service
```

## bluemix resource service-instance
{: #bluemix_resource_service_instance}

サービス・インスタンスの詳細を表示します

```
bluemix resource service-instance NAME [--location LOCATION] [--id]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME (必須)</dt>
  <dd>サービス・インスタンスの名前</dd>
  <dt>--location</dt>
  <dd>場所を基準にフィルター操作します</dd>
  <dt>--id</dt>
  <dd>サービス・インスタンスの ID を表示します</dd>
</dl>

<strong>例</strong>:
サービス・インスタンス `my-service-instance` の詳細を表示します

```
bluemix resource service-instance my-service-instance
```

## bluemix resource service-instance-create
{: #bluemix_resource_service_instance_create}

サービス・インスタンスの作成

```
bluemix resource service-instance-create NAME SERVICE_NAME|SERVICE_ID SERVICE_PLAN_NAME|SERVICE_PLAN_ID LOCATION [-d, --deployment DEPLOYMENT_NAME] [-t, --tags TAGS] [-p, --parameters @JSON_FILE | JSON_STRING ]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME (必須)</dt>
  <dd>サービス・インスタンスの名前</dd>
  <dt>SERVICE_NAME または SERVICE_ID (必須)</dt>
  <dd>サービスの名前または ID</dd>
  <dt>SERVICE_PLAN_NAME または SERVICE_PLAN_ID (必須)</dt>
  <dd>サービス・プランの名前または ID</dd>
  <dt>LOCATION</dt>
  <dd>サービス・インスタンスを作成するターゲットの場所または環境</dd>
  <dt>-t, --tags</dt>
  <dd>タグ</dd>
  <dt>-p, --parameters</dt>
  <dd>サービス・インスタンスを作成するパラメーターの JSON ファイルまたは JSON 文字列</dd>
  <dt>-d, --deployment</dt>
  <dd>デプロイメントの名前</dd>
</dl>

<strong>例</strong>:
場所 `eu-gb` にサービス `test-service` のサービス・プラン `test-service-plan` を使用してサービス・インスタンス `my-service-instance` を作成します。

```
bluemix resource service-instance-create my-service-instance test-service test-service-plan eu-gb
```

## bluemix resource service-instance-update
{: #bluemix_resource_service_instance_update}

サービス・インスタンスを更新します

```
bluemix resource service-instance-update SERVICE_INSTANCE_NAME [-n, --name NEW_NAME] [-t, --tags TAGS] [--service-plan-id SERVICE_PLAN_ID] [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_INSTANCE_NAME (必須)</dt>
  <dd>サービス・インスタンスの名前</dd>
  <dt>-n, --name</dt>
  <dd>新規サービス・インスタンス名</dd>
  <dt>-t, --tags</dt>
  <dd>新規タグ</dd>
  <dt>--service-plan-id</dt>
  <dd>新規サービス・プラン ID</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに更新を強制します</dd>
</dl>

<strong>例</strong>:
サービス・インスタンス `my-service-instance` を更新し、その名前を `new-service-instance` に変更します

```
bluemix resource service-instance-update my-service-instance -n new-service-instance
```

## bluemix resource service-instance-delete
{: #bluemix_resource_service_instance_delete}

サービス・インスタンスを削除します

```
bluemix resource service-instance-delete NAME [-f, --force] [--recursive]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-f, --force</dt>
  <dd>確認なしで削除を強制します</dd>
  <dt>--recursive</dt>
  <dd>従属リソースをすべて削除します</dd>
</dl>

<strong>例</strong>:
リソース・サービス・インスタンス `my-service-instance` を削除します

```
bluemix resource service-instance-delete my-service-instance
```

## bluemix resource service-bindings
{: #bluemix_resource_service_bindings}

サービス別名へのバインディングを表示します

```
bluemix resource service-bindings SERVICE_ALIAS
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ALIAS (必須)</dt>
  <dd>サービス別名</dd>
</dl>

<strong>例</strong>:
サービス別名 `my-service-alias` へのリソース・バインディングを表示します

```
bluemix resource bindings my-service-alias
```
## bluemix resource service-binding
{: #bluemix_resource_service_binding}

サービス・バインディングの詳細を表示します

```
bluemix resource service-binding ALIAS_NAME APP_NAME [--id]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>ALIAS_NAME (必須)</dt>
  <dd>サービス別名</dd>
  <dt>APP_NAME</dt>
  <dd>CloudFoundry アプリケーション名</dd>
  <dt>--id</dt>
  <dd>ID のみを表示します。 このサービス・バインディングの他の出力はすべて抑制されます。</dd>
</dl>

<strong>例</strong>:
サービス別名 `my-service-alias` とアプリ `my-app` の間のサービス・バインディングの詳細を表示します

```
bluemix resource bindings my-service-alias my-app
```

## bluemix resource service-binding-create
{: #bluemix_resource_service_binding_create}

サービス・バインディングの作成

```
bluemix resource service-binding-create SERVICE_ALIAS_NAME APP_NAME ROLE_NAME [--service-id SERVICE_ID] [-p, --parameters @JSON_FILE | JSON_TEXT] [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ALIAS_NAME (必須)</dt>
  <dd>サービス別名</dd>
  <dt>APP_NAME</dt>
  <dd>CloudFoundry アプリケーション名</dd>
  <dt>ROLE_NAME</dt>
  <dd>ユーザー役割の名前</dd>
  <dt>--service-id</dt>
  <dd>役割が属しているサービス ID の名前または UUID</dd>
  <dt>-p, --parameter</dt>
  <dd>パラメーター JSON ファイルまたは JSON 文字列</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに作成を強制します</dd>
</dl>

<strong>例</strong>:
`Administrator` の役割によってサービス別名 `my-service-alias` とアプリ `my-app` の間のサービス・バインディングを作成します

```
bluemix resource service-binding-create my-service-alias my-app Administrator
```
## bluemix resource service-binding-delete
{: #bluemix_resource_service_binding_delete}

サービス・バインディングの削除

```
bluemix resource service-binding-delete SERVICE_ALIAS APP_NAME [-f, --force]
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:
<dl>
  <dt>SERVICE_ALIAS_NAME (必須)</dt>
  <dd>サービス別名</dd>
  <dt>APP_NAME</dt>
  <dd>CloudFoundry アプリケーション名</dd>
  <dt>-f, --force</dt>
  <dd>確認なしで削除を強制します</dd>
</dl>

<strong>例</strong>:
サービス別名 `my-service-alias` とアプリ `my-app` の間のサービス・バインディングを削除します

```
bluemix resource service-binding-delete my-service-alias my-app
```

## bluemix resource service-keys
{: #bluemix_resource_service_keys}

サービス・インスタンスまたはサービス別名のサービス・キーをリストします

```
bluemix resource service-keys [ --instance-id ID | --instance-name NAME | --alias-id ID | --alias-name NAME ]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>--instance-id</dt>
  <dd>サービス・インスタンス ID</dd>
  <dt>--instance-name</dt>
  <dd>サービス・インスタンス名</dd>
  <dt>--alias-id</dt>
  <dd>サービス別名 ID</dd>
  <dt>--alias-name</dt>
  <dd>サービス別名</dd>
</dl>

<strong>例</strong>:
サービス・インスタンス `my-service-instance` のサービス・キーをリストします

```
bluemix resource service-keys --instance-name my-service-instance
```

## bluemix resource service-key
{: #bluemix_resource_service_key}

サービス・キーの詳細を表示します

```
bluemix resource service-key KEY_NAME [--id]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>KEY_NAME</dt>
  <dd>キーの名前</dd>
  <dt>--id</dt>
  <dd>サービス・キーの ID を表示します</dd>
</dl>

<strong>例</strong>:
サービス・キー `my-service-key` の詳細を表示します

```
bluemix resource service-key my-service-key
```

## bluemix resource service-key-create
{: #bluemix_resource_service_key_create}

サービス・キーを作成します

```
bluemix resource service-key-create NAME ROLE_NAME ( --instance-id SERVICE_INSTANCE_ID | --instance-name SERVICE_INSTANCE_NAME | --alias-id SERVICE_ALIAS_ID | --alias-name SERVICE_ALIAS_NAME ) [--service-id SERVICE_ID] [-p, --parameters @JSON_FILE | JSON_TEXT] [-f, --force]]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>NAME</dt>
  <dd>キーの名前</dd>
  <dt>ROLE_NAME</dt>
  <dd>ユーザー役割の名前</dd>
  <dt>--instance-id</dt>
  <dd>サービス・インスタンス ID</dd>
  <dt>--instance-name</dt>
  <dd>サービス・インスタンス名</dd>
  <dt>--alias-id</dt>
  <dd>サービス別名 ID</dd>
  <dt>--alias-name</dt>
  <dd>サービス別名</dd>
  <dt>--service-id</dt>
  <dd>役割が属しているサービス ID の名前または UUID</dd>
  <dt>-p, --parameters</dt>
  <dd>パラメーター JSON ファイルまたは JSON 文字列</dd>
  <dt>-f, --force</dt>
  <dd>確認を求めずに作成を強制します</dd>
</dl>

<strong>例</strong>:
役割 `Administrator` を使用して、サービス・インスタンス `my-service-instance` に対して `my-service-key` という名前のサービス・キーを作成します。

```
bluemix resource service-key-create my-service-key Administrator --instance-name my-service-instance
```

## bluemix resource service-key-delete
{: #bluemix_resource_service_key_delete}

サービス・キーを削除します

```
bluemix resource service-key-delete KEY_NAME [-f, --forece]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>KEY_NAME</dt>
  <dd>キーの名前</dd>
  <dt>-f, --force</dt>
  <dd>確認なしで削除を強制します</dd>
</dl>

<strong>例</strong>:
サービス・キー `my-service-key` を削除します

```
bluemix resource service-key-delete my-service-key
```

## bluemix resource service-aliases
{: #bluemix_resource_service_aliases}

サービス・インスタンスの別名をリストします

```
bluemix resource service-aliases [ --instance-id ID | --instance-name NAME ]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>--instance-id</dt>
  <dd>従属サービス・インスタンスの ID</dd>
  <dt>--instance-name</dt>
  <dd>従属サービス・インスタンスの名前</dd>
</dl>

<strong>例</strong>:
サービス・インスタンス `my-service-instance` のサービス別名をリストします
```
bluemix resource service-aliases my-service-instance
```

## bluemix resource service-alias
{: #bluemix_resource_service_alias}

サービス別名の詳細を表示します

```
bluemix resource service-alias ALIAS_NAME [--id]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>ALIAS_NAME (必須)</dt>
  <dd>サービス別名の名前</dd>
  <dt>--id</dt>
  <dd>指定されたサービス別名の ID のみを表示してください。 この別名の他の出力はすべて抑制されます。</dd>
</dl>

<strong>例</strong>:
サービス別名 `my-service-alias` の詳細を表示します
```
bluemix resource service-alias  my-service-alias
```

## bluemix resource service-alias-create
{: #bluemix_resource_service_alias_create}

サービス・インスタンスの別名を作成します

```
bluemix resource service-alias-create ALIAS_NAME ( --instance-id ID | --instance-name NAME ) [-s SPACE_NAME] [-t, --tags TAGS] [-p, --parameters @JSON_FILE | JSON_TEXT]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>ALIAS_NAME (必須)</dt>
  <dd>サービス別名の名前</dd>
  <dt>--instance-id</dt>
  <dd>従属サービス・インスタンスの ID</dd>
  <dt>--instance-name</dt>
  <dd>従属サービス・インスタンスの名前</dd>
  <dt>-s</dt>
  <dd>別名が作成されるスペースの名前。 デフォルトは現行のスペースです。</dd>
  <dt>-t, --tags</dt>
  <dd>タグのリスト。</dd>
  <dt>-p, --parameters</dt>
  <dd>パラメーター JSON ファイルまたは JSON 文字列。</dd>
</dl>

<strong>例</strong>:
サービス・インスタンス `my-service-instance` のサービス別名 `my-service-alias` を作成します。
```
bluemix resource service-alias-create my-service-alias --instance-name my-service-instance
```

## bluemix resource service-alias-update
{: #bluemix_resource_service_alias_update}

サービス別名を更新します

```
bluemix resource service-alias-update ALIAS_NAME [-n, --name NEW_NAME] [-t, --tags TAGS] [-p, --parameters @JSON_FILE | JSON_STRING ][-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>ALIAS_NAME (必須)</dt>
  <dd>サービス別名の名前</dd>
  <dt>-n, --name</dt>
  <dd>サービス別名の新しい名前。</dd>
  <dt>-t, --tags</dt>
  <dd>タグのリスト。</dd>
  <dt>-p, --parameters</dt>
  <dd>パラメーター JSON ファイルまたは JSON 文字列。</dd>
  <dt>-f, --force</dt>
  <dd>ユーザーの確認を求めずに更新を強制します。</dd>
</dl>

<strong>例</strong>:
サービス別名 `my-service-alias` を更新し、その名前を `new-service-alias` に変更します

```
bluemix resource service-alias-update my-service-alias -n new-service-alias
```

## bluemix resource service-alias-delete
{: #bluemix_resource_service_alias_delete}

サービス別名を削除します

```
bluemix resource service-alias-delete ALIAS_NAME [-f, --force]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>ALIAS_NAME (必須)</dt>
  <dd>サービス別名の名前</dd>
  <dt>-f, --force</dt>
  <dd>確認なしで削除を強制します</dd>
</dl>

<strong>例</strong>:
サービス別名 `my-service-alias` を削除します

```
bluemix resource service-alias-delete my-service-alias
```

## bluemix resource search
{: #bluemix_resource_search}
Lucene 照会構文を使用してリソースを検索します

```
bluemix search LUCENE_QUERY [-o, --offset OFFSET] [-l, --limit LIMIT]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-offset, --o</dt>
  <dd>開始リソース位置番号</dd>
  <dt>-limit, --l</dt>
  <dd>返されるリソースの数 (最大 10000)</dd>
</dl>

<strong>例</strong>:
指定したテキストで始まる名前の Cloud Foundry アプリケーションを検索します。

```
bluemix resource search 'name:my* AND type:cf-application'
```

指定したサービス名の Cloud Foundry サービス・インスタンスを検索します。

```
bluemix resource search 'service_name:messagehub AND type:cf-service-instance'
```

指定した ID を持つ組織内の Cloud Foundry サービス・バインディングを検索します。

```
bluemix resource search 'organization_guid:5b82c134-afb3-4f69-b1e0-3cbe4a13a205 AND type:cf-service-binding'
```

指定した 2 つの地域のどちらかにある、指定した名前の Cloud Foundry スペースを検索します。

```
bluemix resource search 'name:dev AND type:cf-space AND region:(us-south OR eu-gb)'
```

指定した ID の Cloud Foundry スペースの中で、名前に dev が入ったリソースを検索します。

```            
bluemix resource search 'name:*dev* AND doc.space_guid:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7'
```

指定した場所 (つまり us-south 地域) で、リソース・コントローラーのリソースを検索します。

```
bluemix resource search 'region:us-south AND family:resource_controller'
```

指定した ID を持つリソース・グループ内のリソースまたは別名を検索します。

```
bluemix resource search '(type:resource-instance OR type:resource-alias) AND (doc.resource_group_id:c900d9671b235c00461c5e311a8aeced)'
```

デフォルトの名前を持つリソース・グループを検索します。

```
bluemix resource search 'name:default AND type:resource-group'
```

指定したサービス名のリソース・バインディングを検索します。

```
bluemix resource search 'service_name:cloud-object-storage AND type:resource-binding'
```

指定したクラウド・リソース名 (CRN) を持つリソースを検索します。

```
bluemix resource search "crn:\"crn:v1:staging:public:cloudantnosqldb:us-south:s/4948af7e-cc78-4321-998a-e549dd5e9210:41a031cd-e9e5-4c46-975d-9e4a6391322e:cf-service-instance:\""
```

指定したタグを持つリソースを検索します。

```
bluemix resource search "tags:\"mykey:myvalue\""
```

## bluemix catalog search
{: #bluemix_catalog_search}

カタログ項目を検索します

```
bluemix catalog search <QUERY> [-r, --region REGION] [-k, --kind KIND] [-p, --price PRICE] [-t, --tag TAG] [--sort-by PROPERTY] [--col COLUMNS] [--reverse] [--json] [--csv] [--global]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-r, --region</dt>
  <dd>検索範囲の地理的地域を指定します。 現在は、「us-south」と「united-kingdom」のみがサポートされています。</dd>
  <dt>-k, --kind</dt>
  <dd>リソースの種類を基準にしてフィルター操作します。 現在は、「service-cf」、「iaas」、「runtime」、「template」、および「dashboard」のみがサポートされています。</dd>
  <dt>-p, --price</dt>
  <dd>価格を基準にしてフィルター操作します。 現在は、「free」、「paygo」、「bluemix-subscription」のみがサポートされています。</dd>
  <dt>-t, --tag</dt>
  <dd>タグを基準にしてフィルター操作します。</dd>
  <dt>--sort-by</dt>
  <dd>ソート基準のプロパティー</dd>
  <dt>--col</dt>
  <dd>表の追加列を指定します。 現在は、「group」、「provider」、および「 tags」です。</dd>
  <dt>--reverse</dt>
  <dd>ソート順序を反転するかどうか</dd>
  <dt>--json</dt>
  <dd>元の JSON 応答を出力します</dd>
  <dt>--csv</dt>
  <dd>CSV ファイルを出力します</dd>
  <dt>--global</dt>
  <dd>グローバル・スコープで操作します</dd>
</dl>

<strong>例</strong>:

サービス `Automation test` を検索します

```
bluemix catalog search -k service -q 'Automation test'
```


## bluemix catalog entry
{: #bluemix_catalog_entry}

カタログ項目を取得します

```
bluemix catalog entry ID [--global]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>--children</dt>
  <dd>カタログ項目のすべての子を取得します</dd>
  <dt>--json</dt>
  <dd>元の JSON 応答を出力します</dd>
  <dt>--global</dt>
  <dd>グローバル・スコープで操作します</dd>
</dl>

<strong>例</strong>:

ID `a0ef1-d3b4j0` の項目を取得します

```
bluemix catalog entry 'a0ef1-d3b4j0'
```


## bluemix catalog entry-create
{: #bluemix_catalog_entry_create}
新しいカタログ項目を作成します (アカウントのカタログ管理者のみ)

```
bluemix catalog entry-create [-c PARAMETERS_AS_JSON] [-p, --parent PARENT] [--global]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-p, --parent</dt>
  <dd>オブジェクトの親 ID</dd>
  <dt>-c</dt>
  <dd>インラインまたはファイルのいずれかで提供される、カタログ固有の構成パラメーターを含む有効な JSON オブジェクト。 サポートされている構成パラメーターのリストについては、特定のカタログ項目用の資料を参照してください。</dd>
  <dt>--global</dt>
  <dd>グローバル・スコープで操作します</dd>
</dl>

<strong>例</strong>:

親 ID `a0ef1-d3b4j0` を持つ JSON ファイルからリソースを作成します

```
bluemix catalog entry-create -c @entry.json -p 'a0ef1-d3b4j0'
```


## bluemix catalog entry-update
{: #bluemix_catalog_entry_update}
既存のカタログ項目を更新します (アカウントのカタログ管理者またはエディターのみ)

```
bluemix catalog entry-update ID [-c PARAMETERS_AS_JSON] [--global]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-c</dt>
  <dd>インラインまたはファイルのいずれかで提供される、カタログ固有の構成パラメーターを含む有効な JSON オブジェクト。 サポートされている構成パラメーターのリストについては、特定のカタログ項目用の資料を参照してください。</dd>
  <dt>--global</dt>
  <dd>グローバル・スコープで操作します</dd>
</dl>

<strong>例</strong>:

JSON ファイルからリソース `j402-dnf1i` を更新します

```
bluemix catalog entry-update 'j402-dnf1i' -c @update.json
```

## bluemix catalog entry-delete
{: #bluemix_catalog_entry_delete}
カタログ項目を削除します (アカウントのカタログ管理者のみ)
```
bluemix catalog entry-delete ID [--global]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>--global</dt>
  <dd>グローバル・スコープで操作します</dd>
</dl>

<strong>例</strong>:

リソース `j402-dnf1i` を削除します

```
bluemix catalog delete 'j402-dnf1i'
```


## bluemix catalog entry-visibility
{: #bluemix_catalog_entry_visibility}
カタログ項目の可視性を取得します (アカウントのカタログ管理者のみ)

```
bluemix catalog entry-visibility ID [--global]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>-json</dt>
  <dd>元の JSON 応答を出力します</dd>
  <dt>-global</dt>
  <dd>グローバル・スコープで操作します</dd>
</dl>

<strong>例</strong>:

グローバル・スコープでリソース `j402-dnf1i` の可視性を取得します

```
bluemix catalog entry-visibility 'j402-dnf1i' --global
```


## bluemix catalog entry-visibility-set
{: #bluemix_catalog_entry_visibility_set}
既存のカタログ項目の可視性を更新します (アカウントのカタログ管理者のみ)

```
bluemix catalog entry-visibility-set ID [--includes-add LIST] [--includes-remove LIST] [--excludes-add LIST] [--excludes-remove LIST] [--owner ID or Email] [--restrict] [--unrestrict] [-c PARAMETERS_AS_JSON] [--global]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>

  <dt>--includes-add</dt>
  <dd>アカウント (またはコンマ区切りの一連のアカウント) を組み込みリストに追加し、項目の可視性を付与します。 E メールまたはアカウント GUID を指定可能です</dd>
  <dt>--includes-remove</dt>
  <dd>アカウント (またはコンマ区切りの一連のアカウント) を組み込みリストから削除し、項目の可視性を取り消します。 E メールまたはアカウント GUID を指定可能です</dd>  
  <dt>--excludes-add</dt>
  <dd>アカウント (またはコンマ区切りの一連のアカウント) を除外リストに追加します。 E メールまたはアカウント GUID を指定可能です</dd>
  <dt>--excludes-remove</dt>
  <dd>アカウント (またはコンマ区切りの一連のアカウント) を除外リストから削除し、項目の可視性を取り消します。 アカウントがグローバル管理者によって設定されていた場合は、アカウント管理者がそのアカウントを削除することはできません。E メールまたはアカウント GUID を指定可能です</dd>
  <dt>--owner</dt>
  <dd>オブジェクトの所有者を変更します。 E メールまたはアカウント GUID を指定可能です。</dd>
  <dt>--restrict</dt>
  <dd>表示可能オブジェクトの制限を「プライベート」に変更します</dd>
  <dt>--unrestrict</dt>
  <dd>表示可能オブジェクトの制限を「パブリック」に変更します</dd>  
  <dt>-c</dt>
  <dd>インラインまたはファイルのいずれかで提供される、カタログ固有の構成パラメーターを含む有効な JSON オブジェクト。 サポートされている構成パラメーターのリストについては、特定のカタログ項目用の資料を参照してください。</dd>
  <dt>--global</dt>
  <dd>グローバル・スコープで操作します</dd>
</dl>

<strong>例</strong>:

JSON ファイルからリソース `j402-dnf1i` の可視性を設定します

```
bluemix catalog entry-visibility-set 'j402-dnf1i' -c @visibility.json
```


## bluemix catalog service-marketplace
{: #bluemix_catalog_service_marketplace}
マーケットプレイス内のサービス・オファリングをリストします

```
bluemix catalog service-marketplace [--cf] [--rc] [--global]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
<dl>
  <dt>--cf</dt>
  <dd>Cloud Foundry サービスのみを表示します</dd>
  <dt>--rc</dt>
  <dd>RC と互換性のあるサービスのみを表示します</dd>
  <dt>--global</dt>
  <dd>グローバル・スコープで操作します</dd>
</dl>

<strong>例</strong>:

グローバル・スコープでのサービス・オファリングを表示します

```
bluemix catalog service-marketplace --global
```

## bluemix catalog templates
{: #bluemix_catalog_templates}

Bluemix のボイラープレート・テンプレートを表示します。

```
bluemix catalog templates [-d]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>-d (オプション)</dt>
   <dd><i>-d</i> オプションが指定されている場合、各テンプレートの説明
も表示されます。 それ以外の場合、各テンプレートの ID および名前のみが表示されます。</dd>
   </dl>


## bluemix catalog template
{: #bluemix_catalog_template}

指定されたボイラープレート・テンプレートの詳細情報を表示します。

```
bluemix catalog template TEMPLATE_ID
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>TEMPLATE_ID (必須)</dt>
   <dd>ボイラープレート・テンプレートの ID。 すべてのテンプレートの ID を表示するには、
<i>bluemix templates</i> を使用します。</dd>
   </dl>


<strong>例</strong>:

テンプレート `mobileBackendStarter` の詳細を表示します。

```
bluemix catalog template mobileBackendStarter
```


## bluemix catalog template-run
{: #bluemix_catalog_template_run}

指定されたテンプレートをベースにした、指定された URL と説明を持つ cf アプリケーションを作成します。 デフォルトでは、この新規アプリケーションは自動的に開始されます。

```
bluemix catalog template-run TEMPLATE_ID CF_APP_NAME [-u URL] [-d DESCRIPTION] [--no-start]
```

<strong>前提条件</strong>: エンドポイント、ログイン、ターゲット

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>TEMPLATE_ID (必須)</dt>
   <dd>アプリケーションの作成時にそのアプリケーションの基盤とするテンプレート。 すべてのテンプレートの ID を表示するには、<i>bluemix templates</i> を使用します。</dd>
   <dt>CF_APP_NAME (必須)</dt>
   <dd>作成される cf アプリケーションの名前。</dd>
   <dt>-u <i>URL</i> (オプション)</dt>
   <dd>アプリケーションの経路。 指定されない場合、経路は、アプリケーション名およびデフォルト・ドメインに基づいて {{site.data.keyword.Bluemix_notm}} によって自動的に設定されます。</dd>
   <dt>-d <i>DESCRIPTION</i> (オプション)</dt>
   <dd>アプリケーションの説明。</dd>
   <dt>--no-start (オプション)</dt>
   <dd>作成後のアプリケーションを自動的に開始しません。 指定されない場合、アプリケーションは作成された後で自動的に開始されます。</dd>
   </dl>


<strong>例</strong>:

`javaHelloWorld` テンプレートをベースにして cf アプリケーション `my-app` を作成します。

```
bluemix catalog template-run javaHelloWorld my-app
```

`rubyHelloWorld` テンプレートに基づき、経路 `myrubyapp.chinabluemix.net` と説明 `My first ruby app on {{site.data.keyword.Bluemix_notm}}.` を使用してアプリケーション `my-ruby-app` を作成するには、以下のように指定します。

```
bluemix catalog template-run rubyHelloWorld my-ruby-app -u myrubyapp.chinabluemix.net -d "My first ruby app on {{site.data.keyword.Bluemix_notm}}."
```

`pythonHelloWorld` テンプレートをベースにして、自動開始なしでアプリケーション `my-python-app` を作成します。

```
bluemix catalog template-run pythonHelloWorld my-python-app --no-start
```

## bluemix catalog locations
{: #bluemix_catalog_locations}

選択されたフォーマットで地域の選択サブセットを取得します。

```
bluemix catalog locations [-i, --id ID] [-k, --kind KIND] [--col COLUMNS] [--json] [--global] [--csv]
```

<strong>コマンド・オプション</strong>:

<dl>
  <dt>-i, --id</dt>
  <dd>ID でジオグラフィーを指定します。</dd>
  <dt>-k, --kind</dt>
  <dd>指定した種類の項目のリストを取得します。</dd>
  <dt>--col</dt>
  <dd>表の追加列を指定します。 現在は、「group」、「provider」、および「tags」です。</dd>
  <dt>--json</dt>
  <dd>元の JSON 応答の出力。</dd>
  <dt>--global</dt>
  <dd>グローバル・スコープで操作します。</dd>
  <dt>--csv</dt>
  <dd>CSV ファイルを出力します</dd>
</dl>

## bluemix catalog runtime
{: #bluemix_catalog_runtime}

ランタイムの詳細を表示します。このコマンドは、パブリック・クラウドにのみ使用可能です。

```
bluemix catalog runtime RUNTIME_ID
```

<strong>例</strong>:

ランタイム "nodejsHelloWorld" の詳細を表示します。

```
catalog runtime nodejsHelloWorld
```

## bluemix catalog runtimes
{: #bluemix_catalog_runtimes}

すべてのランタイムをリストします。このコマンドは、パブリック・クラウドにのみ使用可能です。

```
bluemix catalog runtimes [-d]
```

<strong>コマンド・オプション</strong>:

<dl>
  <dt>-d</dt>
  <dd>各ランタイムの説明を表示します</dd>
</dl>

<strong>例</strong>:

すべてのランタイムを説明と共にリストします。

```
bluemix catalog runtimes -d
```

## bluemix billing account-usage
{: #bluemix_billing_account_usage}

現行アカウントの月々の使用量を表示します (アカウント管理者のみ)

```
bluemix billing account-usage [-d YYYY-MM] [--json]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:

<dl>
  <dt>-d MONTH_DATE (オプション)</dt>
  <dd>YYYY-MM 形式を使用して指定された日付のデータを表示します。 指定されていない場合、今月の使用量が表示されます。</dd>
  <dt>--json (オプション)</dt>
  <dd>使用量の結果を JSON 形式で表示します。</dd>
</dl>

<strong>例</strong>:

2016 年 6 月の現行アカウントの使用量とコストのレポートを表示します。

```
bluemix billing account-usage -d 2016-06
```

## bluemix billing org-usage
{: #bluemix_billing_org_usage}

組織の月々の使用量を表示します (アカウント管理者または組織の請求管理者のみ)

```
bluemix billing org-usage ORG_NAME [-d YYYY-MM] [--json]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:

<dl>
  <dt>ORG_NAME (必須)</dt>
  <dd>組織の名前。</dd>
  <dt>-d MONTH_DATE (オプション)</dt>
  <dd>YYYY-MM 形式を使用して指定された日付のデータを表示します。 指定されていない場合、今月の使用量が表示されます。</dd>
  <dt>--json (オプション)</dt>
  <dd>使用量の結果を JSON 形式で表示します。</dd>
</dl>


## bluemix billing resource-group-usage
{: #bluemix_billing_resource_group_usage}

リソース・グループの月々の使用量を表示します (アカウント管理者またはリソース・グループ管理者のみ)

```
bluemix billing resource-group-usage GROUP_NAME [-d YYYY-MM] [--json]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:

<dl>
  <dt>GROUP_NAME (必須)</dt>
  <dd>リソース・グループの名前。</dd>
  <dt>-d MONTH_DATE (オプション)</dt>
  <dd>YYYY-MM 形式を使用して指定された日付のデータを表示します。 指定されていない場合、今月の使用量が表示されます。</dd>
  <dt>--json (オプション)</dt>
  <dd>使用量の結果を JSON 形式で表示します。</dd>
</dl>

## bluemix billing resource-instances-usage
{: #bluemix_billing_resource_instances_usage}

現行アカウントの月次リソース・インスタンス使用量を表示します。

```
bluemix billing resource-instances-usage [-o ORG] [-g RESOURCE_GROUP] [-d YYYY-MM] [--json]
```

<strong>前提条件</strong>: エンドポイント、ログイン

<strong>コマンド・オプション</strong>:

<dl>
  <dt>-o ORG_NAME (オプション)</dt>
  <dd>組織を基準にしてインスタンスをフィルターに掛けます。</dd>
  <dt>-g GROUP_NAME</dt>
  <dd>リソース・グループを基準にしてインスタンスをフィルターに掛けます。</dd>
  <dt>-d MONTH_DATE (オプション)</dt>
  <dd>YYYY-MM 形式を使用して指定された日付のデータを表示します。 指定されていない場合、今月の使用量が表示されます。</dd>
  <dt>--json (オプション)</dt>
  <dd>使用量の結果を JSON 形式で表示します。</dd>
</dl>

## bluemix plugin repos
{: #bluemix_plugin_repos}

{{site.data.keyword.Bluemix_notm}} CLI に登録されているすべてのプラグイン・リポジトリーをリストします。

```
bluemix plugin repos
```

<strong>前提条件</strong>: なし


## bluemix plugin repo-add
{: #bluemix_plugin_repo_add}

新規プラグイン・リポジトリーを {{site.data.keyword.Bluemix_notm}} CLI に追加します。

```
bluemix plugin repo-add REPO_NAME REPO_URL
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>REPO_NAME (必須)</dt>
   <dd>追加するリポジトリーの名前。 各リポジトリーに対して任意の名前を定義できます。</dd>
   <dt>REPO_URL (必須)</dt>
   <dd>追加するリポジトリーの URL。 リポジトリー URL にはプロトコルが含まれている必要があります (例えば、plugins.ng.bluemix.net ではなく、http://plugins.ng.bluemix.net)。 {{site.data.keyword.Bluemix_notm}} CLI の公式プラグイン・リポジトリーは http://plugins.ng.bluemix.net です。</dd>
    </dl>


<strong>例</strong>:

{{site.data.keyword.Bluemix_notm}} CLI の公式プラグイン・リポジトリーを `bluemix-repo` として追加します。

```
bluemix plugin repo-add bluemix-repo http://plugins.ng.bluemix.net
```


## bluemix plugin repo-remove
{: #bluemix_plugin_repo_remove}

{{site.data.keyword.Bluemix_notm}} CLI からプラグイン・リポジトリーを削除します。

```
bluemix plugin repo-remove REPO_NAME
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:
   <dl>
   <dt>REPO_NAME (必須)</dt>
   <dd>削除するリポジトリーの名前。</dd>
   </dl>

<strong>例</strong>:

{{site.data.keyword.Bluemix_notm}} CLI から `bluemix-repo` リポジトリーを削除します。

```
bluemix plugin repo-remove bluemix-repo
```


## bluemix plugin repo-plugins
{: #bluemix_plugin_repo_plugins}

追加されたすべてのリポジトリーまたは特定のリポジトリー内にある使用可能なプラグインをすべてリストします。

```
bluemix plugin repo-plugins [-r REPO_NAME]
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>-r <i>REPO_NAME</i> (オプション)</dt>
   <dd>指定されたリポジトリー内のプラグインのみをリストします。</dd>
   </dl>

<strong>例</strong>:

追加されたすべてのリポジトリー内のすべてのプラグインをリストします。

```
bluemix plugin repo-plugins
```

`bluemix-repo` リポジトリー内のすべてのプラグインをリストします。

```
bluemix plugin repo-plugins -r bluemix-repo
```

## bluemix plugin repo-plugin
{: #bluemix_plugin_repo_plugin}

リポジトリー内のプラグインの詳細を表示します。

```
bluemix plugin repo-plugin PLUGIN_NAME [-r REPO_NAME]
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>-r <i>REPO_NAME</i> (オプション)</dt>
   <dd>リポジトリーの名前。 リポジトリーが指定されない場合、コマンドは、デフォルトのプラグイン・リポジトリーを使用します</dd>
   </dl>

<strong>例</strong>:

リポジトリー「sample-repo」内のプラグイン「IBM-Containers」の詳細をリストします

```
bluemix plugin repo-plugin IBM-Containers -r sample-repo
```

デフォルト・リポジトリー内のプラグイン「IBM-Containers」の詳細をリストします

```
bluemix plugin repo-plugin IBM-Containers -r sample-repo
```


## bluemix plugin list
{: #bluemix_plugin_list}

{{site.data.keyword.Bluemix_notm}} CLI 内のインストールされたプラグインをすべてリストします。

```
bluemix plugin list
```

<strong>前提条件</strong>: なし

## bluemix plugin show
{: #bluemix_plugin_show}

インストールされたプラグインの詳細を表示します。

```
bluemix plugin show PLUGIN-NAME
```

<strong>前提条件</strong>: なし


## bluemix plugin install
{: #bluemix_plugin_install}

指定したパスまたはリポジトリーから、特定のバージョンのプラグインを {{site.data.keyword.Bluemix_notm}} CLI にインストールします。

```
bluemix plugin install PLUGIN_PATH|PLUGIN_NAME [-r REPO_NAME] [-v VERSION]
```

```
bx plugin install LOCAL-PATH/TO/PLUGIN | URL [-f]
```

リポジトリーが指定されない場合、コマンドは、デフォルトのプラグイン・リポジトリー「Bluemix」を使用します。
バージョンが指定されない場合、コマンドは、インストール可能な最新バージョンを選択します。

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>PLUGIN_PATH|PLUGIN_NAME (必須)</dt>
   <dd>「-r <i>REPO_NAME</i>」が指定されない場合、指定されたローカル・パスまたはリモート URL からプラグインがインストールされます。</dd>
   <dt>-r <i>REPO_NAME</i> (オプション)</dt>
   <dd>プラグインのバイナリーが配置されているリポジトリーの名前。 リポジトリーが指定されない場合、コマンドは、デフォルトのプラグイン・リポジトリー「Bluemix」を使用します。</dd>
   <dt>-v <i>VERSION</i> (オプション)</dt>
   <dd>インストールするプラグインのバージョン。 指定されていない場合は、最新バージョンのプラグインがインストールされます。 このオプションは、リポジトリーからプラグインをインストールする場合にのみ有効です。</dd>
   <dt>-f </dt>
   <dd>確認なしでプラグインのインストールを強制します。</dd>
    </dl>


{{site.data.keyword.Bluemix_notm}} CLI の公式リポジトリー名は、`Bluemix` です。

<strong>例</strong>:

ローカル・ファイルからプラグインをインストールします。

```
bluemix plugin install /downloads/new_plugin
```

リモート URL からプラグインをインストールします。

```
bluemix plugin install http://plugins.ng.bluemix.net/downloads/new_plugin
```

最新バージョンの「container-service」プラグインを「Bluemix」リポジトリーからインストールするには、以下のように指定します。

```
bluemix plugin install container-service -r Bluemix
```

あるいは、簡単に以下のように指定します。

```
bluemix plugin install container-service
```

公式プラグイン・リポジトリーから、バージョン「0.1.425」の「container-service」プラグインをインストールするには、以下のように指定します。

```
bluemix plugin install container-service -v 0.1.425
```

## bluemix plugin update
{: #bluemix_plugin_update}

リポジトリーからプラグインをアップグレードします。

```
bluemix plugin update [PLUGIN NAME] [-r REPO_NAME] [-v VERSION] [--all]
```

リポジトリーが指定されない場合、コマンドは、デフォルトのプラグイン・リポジトリー「Bluemix」を使用します。
バージョンが指定されない場合、コマンドは、インストール可能な最新バージョンを選択します。

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:
<dl>
 <dt>PLUGIN NAME</dt>
 <dd>更新するプラグインの名前。 指定されない場合、コマンドは、インストールされているすべてのプラグインのアップグレードを確認します。</dd>
 <dt>-r REPO_NAME</dt>
 <dd>プラグインのバイナリーが配置されているリポジトリーの名前。 指定されない場合、コマンドは、デフォルトのプラグイン・リポジトリー「Bluemix」を使用します。</dd>
 <dt>-v <i>VERSION</i> (オプション)</dt>
 <dd>更新するプラグインのバージョン。 表示されない場合、プラグインを入手可能な最新バージョンに更新してください。</dd>
 <dt>--all</dt>
 <dd>利用可能なすべてのプラグインを更新します</dd>
</dl>

<strong>例</strong>:

公式プラグイン・リポジトリー「Bluemix」内のすべての使用可能アップグレードを確認するには、以下のように指定します。

```
bluemix plugin update -r Bluemix
```

あるいは、簡単に以下のように指定します。

```
bluemix plugin update
```

公式プラグイン・リポジトリー内のプラグイン「container-service」を最新にアップグレードするには、以下のように指定します。

```
bluemix plugin update container-service
```

公式プラグイン・リポジトリー内のプラグイン「container-service」をバージョン「0.1.440」に更新するには、以下のように指定します。

```
bluemix plugin update container-service -v 0.1.440
```

## bluemix plugin uninstall
{: #bluemix_plugin_uninstall}

指定されたプラグインを {{site.data.keyword.Bluemix_notm}} CLI からアンインストールします。

```
bluemix plugin uninstall PLUGIN_NAME
```

<strong>前提条件</strong>: なし

<strong>コマンド・オプション</strong>:

   <dl>
   <dt>PLUGIN_NAME (必須)</dt>
   <dd>アンインストールされるプラグインの名前。</dd>
    </dl>

<strong>例</strong>:

前にインストールされた「container-service」プラグインをアンインストールします。

```
bluemix plugin uninstall container-service
```
