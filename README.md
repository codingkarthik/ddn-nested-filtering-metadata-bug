DDN CLI used from [here](https://hasurahq.slack.com/archives/C04NS5JCD8A/p1726496183520129?thread_ts=1726032094.455189&cid=C04NS5JCD8A)
This is a ddn project that was created to test out the nested fields filtering feature:

I ran the following commands:

1. `ddn supergraph init .`
2. `ddn connector init -i` and added the `azure-cosmos` connector.
3. `ddn model add azure_cosmos "*"`
4. `ddn supergraph build local` 

    Running the above step gives the following error:

```✦2 ➜ ddn-cli-new supergraph build local
4:23PM INF Using Supergraph config file "supergraph.yaml" found in context.
4:23PM INF Using localEnvFile ".env" found in context.
4:23PM ERR Code=opendds-validation Message="invalid metadata: error building schema: invalid metadata: an unnecessary filter input type name graphql configuration has been specified for model Scores (in subgraph app) that does not use aggregates"
4:23PM ERR Building Supergraph failed.```
