#!groovy

// imports
import jenkins.model.Jenkins
import hudson.model.ListView
import hudson.views.BuildStatusFilter
import hudson.views.JobStatusFilter
import hudson.views.BuildTrendFilter
import hudson.views.BuildDurationFilter
//import hudson.views.FavoritesFilter
import hudson.views.JobTypeFilter
import hudson.views.ScmTypeFilter
import hudson.views.AddRemoveFallbackFilter
import hudson.views.MostRecentJobsFilter

//import hudson.views.StatusFilter
//def signature = 'new groovy.json.JsonSlurperClassic'
//org.jenkinsci.plugins.scriptsecurity.scripts.ScriptApproval.get().approveSignature(signature)

// get Jenkins instance
Jenkins jenkins = Jenkins.getInstance()

// variables
def viewName = 'Programview10'

// create the new view
jenkins.addView(new ListView(viewName))

// get the view
myView = hudson.model.Hudson.instance.getView(viewName)


//Add BuildStatusFilter
//List<BuildStatusFilter> expectedFilters = new ArrayList<BuildStatusFilter>()
//def filter = new BuildStatusFilter(true,false,false,"includeMatched")
//myView.getJobFilters().add(filter)

//Add StatusFilter
//def filter = new StatusFilter(true)
//myView.getJobFilters().add(filter)

//Add jobstatusfilter
//List<JobStatusFilter> expectedFilters = new ArrayList<JobStatusFilter>()
//def filter = new JobStatusFilter(true,false,false,false,false,"includeMatched")
//myView.getJobFilters().add(filter)

//Add  MostRecentJobsFilter
//List<MostRecentJobsFilter> filtered = new ArrayList<MostRecentJobsFilter>()
//def filter1 = new MostRecentJobsFilter(4,true)
//myView.getJobFilters().add(filter1)

//Add  Job Type Filter
//List<JobTypeFilter> filtered = new ArrayList<JobTypeFilter>()
//def filter = new JobTypeFilter("Freestyle project","includeMatched")
//myView.getJobFilters().add(filter)

//Add  SCM Type Filter
//List<ScmTypeFilter> filtered = new ArrayList<ScmTypeFilter>()
//def filter1 = new ScmTypeFilter("none","includeMatched")
//myView.getJobFilters().add(filter1)

//Add BuildDurationFilter
List<BuildDurationFilter> filtered = new ArrayList<BuildDurationFilter>()
def filter = new BuildTrendFilter("","","","","","includeMatched")
myView.getJobFilters().add(filter)

//Add Build Trend Filter
//List<BuildTrendFilter> filtered = new ArrayList<BuildTrendFilter>()
//def filter = new BuildTrendFilter("","","","","")
//def filter = new BuildTrendFilter("","","","","includeMatched")
//myView.getJobFilters().add(filter)

//Add Fallback Filter
//List<AddRemoveFallbackFilter> filtered = new ArrayList<AddRemoveFallbackFilter>()
//def filter = new AddRemoveFallbackFilter("Remove all jobs if all jobs are included")
//myView.getJobFilters().add(filter)

//Add Favorites Filter
//List<AddRemoveFallbackFilter> filtered = new ArrayList<AddRemoveFallbackFilter>()
//def filter = new FavoritesFilter()
//myView.getJobFilters().add(filter)



// save current Jenkins state to disk
jenkins.save()

