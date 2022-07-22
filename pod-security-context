#!/bin/sh

# List all security contexts for all pods in all namespaces

kubectl get pods --all-namespaces -o go-template --template='{{range .items}}{{"Pod Name: "}}{{.metadata.name}}
    {{if .spec.securityContext}}
      PodSecurityContext:
        {{"runAsGroup: "}}{{.spec.securityContext.runAsGroup}}                               
        {{"runAsNonRoot: "}}{{.spec.securityContext.runAsNonRoot}}                           
        {{"runAsUser: "}}{{.spec.securityContext.runAsUser}}                                 {{if .spec.securityContext.seLinuxOptions}}
        {{"seLinuxOptions: "}}{{.spec.securityContext.seLinuxOptions}}                       {{end}}
    {{else}}PodSecurity Context is not set
    {{end}}{{range .spec.containers}}
    {{"container name: "}}{{.name}}
    {{"image: "}}{{.image}}{{if .securityContext}}                                      
        {{"allowPrivilegeEscalation: "}}{{.securityContext.allowPrivilegeEscalation}}   {{if .securityContext.capabilities}}
        {{"capabilities: "}}{{.securityContext.capabilities}}                           {{end}}
        {{"privileged: "}}{{.securityContext.privileged}}                               {{if .securityContext.procMount}}
        {{"procMount: "}}{{.securityContext.procMount}}                                 {{end}}
        {{"readOnlyRootFilesystem: "}}{{.securityContext.readOnlyRootFilesystem}}       
        {{"runAsGroup: "}}{{.securityContext.runAsGroup}}                               
        {{"runAsNonRoot: "}}{{.securityContext.runAsNonRoot}}                           
        {{"runAsUser: "}}{{.securityContext.runAsUser}}                                 {{if .securityContext.seLinuxOptions}}
        {{"seLinuxOptions: "}}{{.securityContext.seLinuxOptions}}                       {{end}}{{if .securityContext.windowsOptions}}
        {{"windowsOptions: "}}{{.securityContext.windowsOptions}}                       {{end}}
    {{else}}
        SecurityContext is not set
    {{end}}
{{end}}{{end}}'
